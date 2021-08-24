---
description: Características de administración de un dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: CIM_USBDevice (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3766d6c2fdc46b36350e9259e0e988f3a276cee6376d02de349abbe83bf8031b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427735"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>CIM_USBDevice (administración de Hyper-V)

Características de administración de un dispositivo USB.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM USBDevice** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ USBDevice** de CIM tiene estos métodos.



| Método                                               | Descripción                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Recupera un descriptor de dispositivo USB.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ CIM USBDevice** tiene estas propiedades.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceClass")
</dt> </dl>

Código de clase USB.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de tiempo de espera que pueden configurar las aplicaciones de administración que admiten el redireccionamiento USB. Cuando el servicio de redireccionamiento redirige un comando de dispositivo USB a un dispositivo remoto y el dispositivo remoto no responde antes del intervalo de tiempo de espera, el servicio de redirección emulará un evento de expulsión de medios. Además, el servicio puede volver a intentar el comando o intentar restablecer la conexión al dispositivo remoto.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")
</dt> </dl>

Matriz que contiene la configuración alternativa para cada interfaz de la configuración actual del dispositivo.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")
</dt> </dl>

Configuración seleccionada actualmente para el dispositivo. Si este valor es cero, el dispositivo no está configurado.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bcdDevice")
</dt> </dl>

Número de versión del dispositivo en formato BCD.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iManufacturer")
</dt> </dl>

Cadena de fabricante del dispositivo.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bMaxPacketSize")
</dt> </dl>

Tamaño máximo del paquete para el punto de conexión usb cero.

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bNumConfigurations")
</dt> </dl>

Número de configuraciones de dispositivo definidas para el dispositivo.

</dd> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iProduct")
</dt> </dl>

Cadena de producto del dispositivo.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| idProduct")
</dt> </dl>

Identificador de producto asignado al dispositivo por fabricante.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceProtocol")
</dt> </dl>

El código del protocolo USB.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iSerialNumber")
</dt> </dl>

El número de serie del dispositivo.

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceSubClass")
</dt> </dl>

Código de subclase USB.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión usb más reciente compatible con el dispositivo USB. La propiedad se expresa como un decimal codificado binariamente (BCD) que contiene un separador decimal entre los dígitos 2 y 3. Por ejemplo, un valor de 0x201 indica que se admite la versión 2.01.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bcdUSB")
</dt> </dl>

Número de especificación USB con el que cumple el dispositivo. Esta propiedad tiene el formato BCD.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| idVendor")
</dt> </dl>

Identificador de proveedor asignado al dispositivo por USB.org.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> </dl>

 

