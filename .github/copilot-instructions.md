# GitHub Copilot Instruction for 21st Century Arsenal (Continued) Mod

### Mod Overview and Purpose
The **21st Century Arsenal (Continued)** mod is designed to integrate a lore-friendly selection of modern firearms from the 21st century into RimWorld. Drawing inspiration from around the globe, the mod features an expanding roster of firearms including rifles, pistols, shotguns, sniper rifles, and more. The mod aims to provide a balanced and immersive experience for players who are interested in modern weaponry, all while maintaining compatibility with existing game saves. The purpose of the mod is to enrich gameplay by offering varied combat options that are grounded in real-world firearm designs.

### Key Features and Systems
- **Variety of Weapons**: Currently featuring 18 unique weapons across 7 categories such as assault rifles, sniper rifles, light machine guns, and more, drawing from real-world designs from the 21st century.
- **Production and Research**: All weapons can be crafted at the Machining Table and require corresponding research progress via Gunsmithing, Blowback Operation, Gas Operation, and Precision Rifling techs.
- **Modular Compatibility**: Compatible with existing game saves and capable of integrating with other mods for expanded functionality, such as Proper Shotguns if it is loaded.
- **Continual Development**: The mod is actively being developed with plans to expand up to 59 different weapons.

### Coding Patterns and Conventions
- **XML Definitions**: Weapons and bullets use XML configuration for data-driven design, ensuring flexibility and easy updates.
  - Common XML format for weapon and bullet definitions using `<ThingDef>` with inheritance from base definitions (`BaseBullet` and `BaseHumanMakeableGun`).
- **Comprehensive Def Files**: All weapons have associated XML files with consistent naming conventions (e.g., `AR_ACR.xml` for an Assault Rifle).

### XML Integration
- **XML Structure**: Each weapon is defined in its own XML file under the `<Defs>` tag, using a standardized inheritance pattern from base definitions.
- **Bullet and Gun Integration**: All weapons integrate a `<ThingDef>` for their bullets, often paired with a separate `<ThingDef>` for the weapon itself.
- **Damage Handling**: Weapon damage is specified through the `<damageDef>` tag within bullet definitions, allowing refined control over damage types.

### Harmony Patching
- **C# Harmony Requirement**: The mod currently does not utilize C# or Harmony patching, relying entirely on XML definitions for its content.
- **Potential for Expansion**: Future updates could implement Harmony patches for advanced functionality, dynamic modifications, or integration with other mods beyond what XML offers.

### Suggestions for GitHub Copilot
- **XML Automation**: Use Copilot to streamline the creation of XML files by auto-completing repetitive tags and inheriting from standard base definitions.
- **Def Consistency**: Ensure that all weapon definitions utilize consistent structure and style in XML files for seamless integration and error minimization.
- **Error Reporting Guidance**: Provide in-document guidance on proper logging and debugging practices when issues arise, facilitating efficient troubleshooting.
- **Documentation**: Automatically generate documentation snippets based on the XML structure, giving developers and users an insightful reference to the mod's configurations.

### Community and Additional Support
- Feedback is appreciated and can be provided through the comments section or the RimWorld community Discord at `@Axi#9143`.
- Use the log uploader for error reporting and refer to the recommended Discord-channel for support.
- Avoid posting errors in discussion threads as they may go unnoticed.

This mod aims to be a collaborative project, inviting contributions, and suggestions for weapons, balance tweaks, and general functionality improvements.

## Project Solution Guidelines
- Relevant mod XML files are included as Solution Items under the solution folder named XML, these can be read and modified from within the solution.
- Use these in-solution XML files as the primary files for reference and modification.
- The `.github/copilot-instructions.md` file is included in the solution under the `.github` solution folder, so it should be read/modified from within the solution instead of using paths outside the solution. Update this file once only, as it and the parent-path solution reference point to the same file in this workspace.
- When making functional changes in this mod, ensure the documented features stay in sync with implementation; use the in-solution `.github` copy as the primary file.
- In the solution is also a project called Assembly-CSharp, containing a read-only version of the decompiled game source, for reference and debugging purposes.
- For any new documentation, update this copilot-instructions.md file rather than creating separate documentation files.
