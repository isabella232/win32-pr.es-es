---
description: Representa el estado del puerto PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Msvm_PciExpress clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db30d367cbecd0e7b235000a35da26f5baaa07f1c05d0160a9b0bb23c7cfc2c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811221"
---
# <a name="msvm_pciexpress-class"></a>Clase PciExpress de Msvm \_

Representa el estado del puerto PCI Express.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a>Miembros

La **clase \_ PciExpress de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PciExpress de Msvm** tiene estas propiedades.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que contiene la ruta de acceso de la instancia del dispositivo que identifica el dispositivo PCI Express virtual del dispositivo.

</dd> <dt>

**FunctionNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de función del dispositivo PCI Express virtual.

</dd> <dt>

**LocationPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que contiene la ruta de acceso de ubicación del dispositivo que identifica el dispositivo PCI Express virtual del dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




