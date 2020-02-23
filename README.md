# alexandria
A starter FileMaker system with various built-in modules and custom functions.

Username: Developer
Password: developer

## Scripts

### Templates

#### `Script Template`

- Standard header comment with lines for purpose, parameters, return value, version, and notes
- Defaults script beginning with `Allow User Abort [ Off ]`
- Standard `If` block that assigns script parameters to variables and an inner `If` block to test for use of the `funit` module
- Standard `Exit Script` step with a return value indicating success.

#### `PSoS Template`

- Same defaults as above, but also has structure to recursively call itself on the server and execute locally if there's an problem doing so

#### `module` folder

- Starter scripts for a new module with standard folders for configuration, testing, public interface scripts, and private scripts

### Triggers

- One script for each potential trigger, with optional `Sender` parameter so each can branch based on the trigger's sender
- Includes comments in each header to document the meaning of `True` and `False` return values.

### Modules

- `accounts`: Allows scripted account management and forgotten password feature
- `audit-log`: Allows automatic logging of changes and the ability to create custom log entries
- `dialog`: Scripts to show dynamic custom dialogs and to use dimmed card windows as dialog boxes
- `files`: Abstraction of file functions, such as reading and writing files
- `funit`: Enable automatic testing of scripts and custom functions
- `primary-key`: A module used by other modules that need to know the primary key field for tables
- `project`: Scripts facilitating management of a FileMaker project, especially one that's open source
- `slack-bot`: Uses the Slack API to send messages and files to Slack users
- `utilities`: Various useful scripts that don't fit in other modules
- `window`: Create windows of various sorts, such as centered card windows or offscreen utility windows

## Custom Function Sets

- `const`: Constants used by FileMaker such as those for use with the `Sort` function
- `container`: Functions to deal with container field contents
- `crypt`: One function to create a hex digets with a single call
- `data`: Commonly needed data constants, such as digits or weekdays
- `date`: Functions for working with dates
- `dev`: Functions useful to developers
- `err`: Error number constants
- `geo`: A single function to calculate the distance between geographic coordinates
- `housekeeping`: Functions that will suspend and resume the updating of housekeeping functions
- `json`: Functions that ease dealing with JSON
- `key`: Unicode character constants and codes
- `let`: Let-notation functions
- `list`: List manipulation functions
- `log`: Single function to create a fairly complete let-notation system state
- `math`: Functions dealing with math operations
- `mode`: Constant functions representing FileMaker's various modes
- `modifier`: Functions to ease working with keyboard modifier checks
- `msg: Constants for various dialog messages
- `path`: Path manipulation functions
- `platform`: Functions to ease platform checks
- `range`: Functions to generate integer or date ranges
- `repeat`: Functions to assist the repeat module
- `rgb`: RGB values for various common colors
- `schema`: Functions to ease introspection of the file's schema
- `script`: Functions to deal with sending and parsing script parameters
- `sortable`: Functions to translate various data into data sortable by text
- `sql`: Functions to ease dealing with SQL queries
- `system`: Constants related to the system state
- `text`: Functions for dealing with text and text parsing
- `timestamp`: Functions for dealing with timestamps
- `triggers`: Functions to suspend and resume script triggers
- `url`: URL manipulation functions
- `window`: Window management and positioning functions
- `xml`: Single function for extracting data from XML
