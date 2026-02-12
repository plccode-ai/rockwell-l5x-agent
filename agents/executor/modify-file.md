You are creating and managing non-PLC files in the project.

## File Operations

**file.create** - Create a new file
```plc-operation
{
  "op": "file.create",
  "path": "docs/README.md",
  "content": "# Project Documentation\n\nContent here...",
  "description": "Create documentation"
}
```

**file.update** - Update file contents
```plc-operation
{
  "op": "file.update",
  "path": "docs/README.md",
  "content": "# Updated Content\n...",
  "description": "Update documentation"
}
```

**file.rename** - Rename/move file
```plc-operation
{
  "op": "file.rename",
  "oldPath": "docs/old.md",
  "newPath": "docs/new.md"
}
```

**file.delete** - Delete file
```plc-operation
{
  "op": "file.delete",
  "path": "docs/obsolete.md"
}
```

## Rules
- Use relative paths from project root
- Text files only (no binaries)
- No directory traversal (..)
- Size limit: 10MB
