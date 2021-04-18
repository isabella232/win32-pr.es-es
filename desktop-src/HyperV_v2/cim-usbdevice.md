---
description: Las características de administración de un dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: CIM_USBDevice (clase, administración de Hyper-V)
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
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687347"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>CIM_USBDevice (clase, administración de Hyper-V)

Las características de administración de un dispositivo USB.

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

La clase **CIM \_ USBDevice** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **CIM \_ USBDevice** tiene estos métodos.



| Método                                               | Descripción                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Recupera un descriptor de dispositivo USB.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **CIM \_ USBDevice** tiene estas propiedades.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bDeviceClass")
</dt> </dl>

Código de la clase USB.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un intervalo de tiempo de espera que pueden configurarse las aplicaciones de administración que admiten el redireccionamiento USB. Cuando el servicio de redirección redirige un comando de dispositivo USB a un dispositivo remoto, y el dispositivo remoto no responde antes del intervalo de tiempo de espera, el servicio de redireccionamiento emulará un evento de expulsión de medios. Además, el servicio puede volver a intentar el comando o intentar volver a establecer la conexión con el dispositivo remoto.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")
</dt> </dl>

Una matriz que contiene la configuración alternativa para cada interfaz en la configuración actual del dispositivo.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")
</dt> </dl>

La configuración seleccionada actualmente para el dispositivo. Si este valor es cero, el dispositivo no está configurado.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bcdDevice")
</dt> </dl>

El número de versión del dispositivo en formato BCD.

</dd> <dt>

**Le**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| iManufacturer")
</dt> </dl>

Cadena del fabricante del dispositivo.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bMaxPacketSize")
</dt> </dl>

El tamaño máximo del paquete para el extremo de cero USB.

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bNumConfigurations")
</dt> </dl>

El número de configuraciones de dispositivo definidas para el dispositivo.

</dd> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| iProduct")
</dt> </dl>

Cadena de producto del dispositivo.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| idProduct")
</dt> </dl>

El ID. de producto asignado al dispositivo por fabricante.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bDeviceProtocol")
</dt> </dl>

Código del protocolo USB.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| iSerialNumber")
</dt> </dl>

El número de serie del dispositivo.

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bDeviceSubClass")
</dt> </dl>

Código de la subclase USB.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión USB más reciente compatible con el dispositivo USB. La propiedad se expresa como un decimal con codificación binaria (BCD) que contiene un separador decimal entre el segundo y el tercer dígito. Por ejemplo, un valor de 0x201 indica que se admite la versión 2,01.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bcdUSB")
</dt> </dl>

El número de especificación USB que el dispositivo cumple. Esta propiedad tiene el formato BCD.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| idVendor")
</dt> </dl>

El identificador de proveedor asignado al dispositivo por USB.org.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

