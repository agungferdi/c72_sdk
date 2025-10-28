# Chainway C72 RFID Reader - Complete API Documentation

## Project Overview
**Device**: Chainway C72 Handheld RFID Reader
**Generation Date**: Mon Nov 25 17:26:07 CST 2024
**Documentation Type**: Javadoc API Reference
**Repository**: https://github.com/agungferdi/c72_sdk

---

## 📦 Package Structure

### Core Packages

#### 1. **com.rscja** (Root Package)
- **CWDeviceInfo**: Core device information class
- Main entry point for device operations

#### 2. **com.rscja.barcode** - Barcode Operations
**Classes**:
- `Barcode1D`: Handles 1D barcode scanning
- `Barcode2D`: Handles 2D barcode scanning
- `BarcodeDecoder`: Decodes barcode data with callback interface
- `BarcodeFactory`: Factory for creating barcode instances
- `BarcodeUtility`: Utility functions for barcode operations
- `BarcodeSymbolUtility`: Symbol configuration utilities
- `IBarcode2DSHardwareInfo`: Hardware information interface

**Key Interfaces**:
- `BarcodeDecoder.DecodeCallback`: Callback for barcode decode events
- `BarcodeDecoder.IBarcodeImageCallback`: Image processing callback

#### 3. **com.rscja.custom** - Custom RFID Implementations
**RFID Classes**:
- `M775Authenticate`: M775 authentication protocol
- `RFIDWithUHFJieCe`: UHF RFID JieCe implementation
- `UHFCSYX`: UHFCSYX protocol support
- `UHFCSYXForURx`: URx network support
- `UHFTamperAPI`: Tamper detection API
- `UHFTemperatureSensors`: Temperature sensing capabilities
- `UHFTemperatureTagsAPI`: Temperature tag management
- `UHFUartFoxconn`: UART Foxconn protocol
- `UHFXSAPI`: XS protocol support

**Temperature Tag Support**:
- `UHFTemperatureTag`: Base temperature tag interface
- `RFIDWithUHFBLEN51`: Bluetooth LE tag support
- `RFIDWithUHFBLEN52`: Enhanced Bluetooth LE tag support

#### 4. **com.rscja.deviceapi** - Device API Interfaces
**Core Interfaces**:
- `IReader`: Base reader interface
- `IModule`: Module interface
- `IHandheldRFID`: Handheld RFID operations
- `IRFIDBase`: RFID base operations

**RFID Protocol Interfaces**:
- `IUHF`: General UHF interface
- `IUHFA4`: UHF A4 antenna support
- `IUHFA8`: UHF A8 antenna support
- `IRFIDWithUHFA4`: A4 implementation
- `IRFIDWithUHFA8`: A8 implementation
- `IRFIDWithUHFA4NetWork`: Network support for A4
- `IRFIDWithUHFA8NetWork`: Network support for A8
- `IRFIDWithUHFA4RS232`: Serial RS232 for A4
- `IRFIDWithUHFA8RS232`: Serial RS232 for A8
- `IRFIDWithUHFA4Uart`: UART for A4
- `IRFIDWithUHFA8Uart`: UART for A8
- `IRFIDWithUHFRLM`: RLM module support
- `IRFIDWithUHFUSB`: USB connection support
- `IRFIDWithUHFUrxNetwork`: URx network protocol
- `IRFIDWithUHFUrxUart`: URx UART protocol
- `IRFIDWithUHFUrxUsbToUart`: URx USB-to-UART adapter

**HF (High Frequency) Interfaces**:
- `IHF14443A`: ISO14443A protocol
- `IHF14443B`: ISO14443B protocol
- `IHF15693`: ISO15693 protocol
- `IRFIDWithISO14443A`: ISO14443A implementation
- `IRFIDWithISO14443B`: ISO14443B implementation
- `IRFIDWithISO15693`: ISO15693 implementation
- `IRFIDWithISO14443A4CPU`: ISO14443A4 CPU card support
- `IRFIDWithLF`: Low Frequency support

**Barcode Interfaces**:
- `IBarcode1D`: 1D barcode interface
- `IBarcode2D`: 2D barcode interface
- `IBarcodeUtility`: Barcode utilities
- `IBarcodeSymbolUtility`: Barcode symbols
- `IBarcodePhoto`: Photo barcode processing
- `IBarcodePictureCallback`: Picture callback
- `IBarcodeVideoCallback`: Video callback

**Hardware Control**:
- `ILedLight`: LED light control
- `IScanerLedLight`: Scanner LED control
- `IInfrared`: Infrared control
- `IPrinter`: Printer interface
- `IPSAM`: PSAM card interface

**Connectivity**:
- `IBluetoothReader`: Bluetooth reader interface
- `IBleDevice`: BLE device interface
- `IBluetoothData`: Bluetooth data interface
- `IUhfBle`: UHF Bluetooth support

**Callbacks and Listeners**:
- `IUHFInventoryCallback`: Inventory scan callback
- `IUHFLocationCallback`: Location callback
- `ITagLocationCallback`: Tag location callback
- `ITagLocate`: Tag location interface
- `ConnectionStatusCallback`: Connection status events
- `IConnectionStatusChangedListener`: Connection listener
- `OnLowBatteryListener`: Battery warning listener
- `KeyEventCallback`: Key event callback
- `ScanBTCallback`: Scan Bluetooth callback

**Other Utilities**:
- `IFingerprint`: Fingerprint scanning
- `IFingerprintWithFIPS`: FIPS fingerprint
- `IFingerprintWithMorpho`: Morpho fingerprint
- `IFingerprintWithZAZ`: ZAZ fingerprint
- `IFingerprintSM206B`: SM206B fingerprint
- `IUsbFingerprint`: USB fingerprint interface
- `IUpgradeProgress`: Firmware upgrade tracking

#### 5. **com.rscja.deviceapi.entity** - Data Entities
Entity classes for data transfer and storage

#### 6. **com.rscja.deviceapi.enums** - Enumerations
Enum definitions for various device states and configurations

#### 7. **com.rscja.deviceapi.exception** - Exception Classes
Custom exception definitions for error handling

#### 8. **com.rscja.deviceapi.interfaces** - Extended Interfaces
Additional interface definitions for device operations

#### 9. **com.rscja.scanner** - Scanner Operations
- `IScanner`: Scanner interface
- `OnUhfWorkStateListener`: UHF work state listener

#### 10. **com.rscja.scanner.led** - Scanner LED Control
- `ScanLed`: Scanner LED control class
- `ScanLedManage`: LED management

#### 11. **com.rscja.scanner.utility** - Scanner Utilities
- `ScannerUtility`: Scanner utility functions

#### 12. **com.rscja.system** - System Operations
- `ISystemInterfaces`: System interface provider
- `SystemInterfacesFactory`: Factory for system interfaces

#### 13. **com.rscja.utility** - General Utilities
- `BatteryUtils`: Battery management utilities
- `FileUtility`: File operations
- `FingerprintPictureUtility`: Fingerprint image handling
- `NetUtils`: Network utilities
- `NumberTool`: Number conversion utilities
- `StringUtility`: String manipulation utilities
- `UhfUtils`: UHF-specific utilities

#### 14. **com.rscja.team.mtk** - MTK Platform Implementation
MediaTek-specific device implementations
- `DeviceConfiguration_mtk`: MTK device configuration
- Barcode, RFID, Scanner, System implementations for MTK

#### 15. **com.rscja.team.qcom** - Qualcomm Platform Implementation
Qualcomm-specific device implementations
- `DeviceConfiguration_qcom`: QCom device configuration
- Comprehensive implementations for:
  - Barcode scanning (including multiple symbol providers)
  - RFID operations (UHF, HF, etc.)
  - BLE connectivity
  - Serial port communication
  - HTTP utilities
  - UHF protocol parsing
  - Socket communication
  - USB operations
  - Device-specific utilities

---

## 🔑 Key Features

### RFID Capabilities
- **UHF (Ultra High Frequency)** support with multiple antenna configurations (A4, A8, RLM)
- **HF (High Frequency)** support for ISO standards (14443A, 14443B, 15693)
- **Multiple Communication Interfaces**: USB, RS232, UART, Bluetooth, Network
- **Temperature Sensing**: Temperature tag support with BLE connectivity
- **Authentication**: M775 authentication protocol support
- **Custom Protocols**: JieCe, CSYX, XS protocols

### Barcode Scanning
- **1D and 2D barcode** support
- **Hardware-accelerated** decoding
- **Symbol configuration** for various barcode formats
- **Image and video** processing callbacks
- **Keyboard emulation** for barcode input

### Device Control
- **LED Light Control**: Customizable LED indicators
- **Scanner LED Management**: Scan-specific LED patterns
- **Infrared Control**: IR operations
- **Printer Interface**: Integrated thermal printing
- **PSAM Card** support for secure operations

### Biometric Features
- **Fingerprint Scanning**: Multiple vendor support
  - FIPS-certified fingerprints
  - Morpho fingerprint scanners
  - SM206B fingerprints
  - ZAZ fingerprints
- **USB Fingerprint** devices

### Connectivity
- **Bluetooth/BLE**: Wireless RFID operations
- **Network**: TCP/IP communications
- **Serial Communication**: RS232, UART support
- **USB**: Direct USB connectivity

### System Integration
- **Battery Management**: Low battery notifications
- **Firmware Upgrade**: Progress tracking
- **Key Events**: Hardware button handling
- **Connection Status**: Real-time connection monitoring
- **Device Configuration**: Platform-specific settings (MTK, QCom)

---

## 📊 Platform Support

### MediaTek (MTK) Platform
- Device configuration and initialization
- Barcode scanning with multiple symbol types
- RFID operations with antenna selection
- Scanner LED management
- System property management
- Utility functions specific to MTK

### Qualcomm (QCom) Platform
- Extended device configuration
- Advanced barcode symbol support (CoAsia, Honeywell, Idata, MobyData, Zebra)
- Comprehensive UHF protocol parsing
- BLE and UART enhancements
- Network socket support
- HTTP utilities
- Multiple scanner LED configurations for different device models
- Enhanced security and diagnostics

---

## 🔌 Communication Protocols

### RFID Protocols
- **UHF**: Multiple antenna systems, network support, UART/RS232 interfaces
- **HF**: ISO 14443A/B, ISO 15693 standards
- **LF**: Low frequency support
- **BLE**: Bluetooth Low Energy for wireless tags

### Barcode Protocols
- **1D Standards**: Multiple standard support
- **2D Standards**: QR, DataMatrix, PDF417, etc.
- **Keyboard Emulation**: Direct system input
- **Image/Video**: Real-time processing

### Serial Communication
- **RS232**: Serial port connectivity
- **UART**: UART protocol support
- **USB**: USB device support with PL2302 adapter

---

## 📝 Usage Pattern Examples

### Basic Device Access
```
1. Get SystemInterfaces from factory
2. Access desired API (Barcode1D, RFID, etc.)
3. Register callbacks for events
4. Execute operations
5. Handle responses through callbacks
```

### Barcode Scanning
```
1. Get Barcode1D or Barcode2D instance
2. Implement DecodeCallback
3. Start scan operation
4. Receive barcode data through callback
5. Process results
```

### RFID Inventory
```
1. Get IRFIDWithUHFA4 or similar interface
2. Implement IUHFInventoryCallback
3. Execute inventory operation
4. Receive tag data through callback
5. Process tag information
```

### Temperature Monitoring
```
1. Get UHFTemperatureTagsAPI instance
2. Start temperature tag inventory
3. Receive temperature data with tag info
4. Log or process temperature data
```

---

## 🔍 API Reference Quick Links

### Main Entry Points
- Device Info: `com.rscja.CWDeviceInfo`
- System Factory: `com.rscja.system.SystemInterfacesFactory`
- Barcode Factory: `com.rscja.barcode.BarcodeFactory`

### Common Callbacks
- Barcode Decode: `BarcodeDecoder.DecodeCallback`
- RFID Inventory: `IUHFInventoryCallback`
- Connection Status: `ConnectionStatusCallback`
- Battery: `OnLowBatteryListener`

### Configuration Classes
- MTK Config: `com.rscja.team.mtk.DeviceConfiguration_mtk`
- QCom Config: `com.rscja.team.qcom.DeviceConfiguration_qcom`

---

## 📱 Supported Devices

The SDK supports Chainway C72 and related handheld RFID readers across:
- **MediaTek (MTK)** platform
- **Qualcomm (QCom)** platform (with enhanced features)

Device models include various configurations supporting:
- C60 series
- C61 series
- C66 series
- C66m series
- C72 series
- MC50 series
- P80 series

---

## 🛠️ Error Handling

All major operations include:
- Exception classes in `com.rscja.deviceapi.exception`
- Status callbacks for operation results
- Connection status monitoring
- Battery level warnings

---

## 📚 Documentation Structure

All documentation files are located in the `/doc` directory and organized by package:
- `/doc/com/rscja/` - Main SDK documentation
- `/doc/com/rscja/barcode/` - Barcode APIs
- `/doc/com/rscja/custom/` - Custom RFID implementations
- `/doc/com/rscja/deviceapi/` - Core device APIs
- `/doc/com/rscja/scanner/` - Scanner control
- `/doc/com/rscja/system/` - System management
- `/doc/com/rscja/team/mtk/` - MTK platform specifics
- `/doc/com/rscja/team/qcom/` - QCom platform specifics
- `/doc/com/rscja/utility/` - Utility functions
- `/doc/index-files/` - Searchable index

---

## 🌐 Access Information

**Live Documentation**: https://c72-sdk.vercel.app/
**Source Repository**: https://github.com/agungferdi/c72_sdk
**Device Manufacturer**: Chainway Technology

---

## 📖 How to Use This Documentation

1. **For Overview**: Start at `overview-summary.html`
2. **For All Classes**: Visit `allclasses-noframe.html`
3. **For Specific Package**: Browse the package directories in `/doc/com/rscja/`
4. **For Method Details**: Click on specific class documentation files
5. **For Search**: Use `index-files/index-*.html` for alphabetical index

---

**Last Updated**: October 28, 2025
**Documentation Version**: 20250209
**Java Version**: 1.8.0_302
