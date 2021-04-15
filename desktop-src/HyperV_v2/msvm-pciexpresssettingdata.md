---
description: Representa el estado configurado de un puerto PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Msvm_PciExpressSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688555"
---
# <a name="msvm_pciexpresssettingdata-class"></a>MSVM \_ PciExpressSettingData (clase)

Representa el estado configurado de un puerto PCI Express.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ PciExpressSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ PciExpressSettingData** tiene estas propiedades.

<dl> <dt>

**VirtualFunctions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número de función virtual que se va a asignar a la máquina virtual.

</dd> <dt>

**VirtualSystemIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Matriz de cadenas de formato libre de los identificadores de este recurso presentados al sistema operativo del sistema del equipo virtual. Los índices y valores por índice se definen por cada recurso (es decir, por cada valor **resourcetype** enumerado). Esta propiedad se establece en "GUID".

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) de la clase SD.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

