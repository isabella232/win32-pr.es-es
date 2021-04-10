---
description: Describe los datos de configuración para un puerto serie virtual.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Msvm_SerialPortSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910130"
---
# <a name="msvm_serialportsettingdata-class"></a>MSVM \_ SerialPortSettingData (clase)

Describe los datos de configuración para un puerto serie virtual.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SerialPortSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SerialPortSettingData** tiene estas propiedades.

<dl> <dt>

**DebuggerMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**true** si el modo del depurador está habilitado en un puerto serie virtual; en caso contrario, **false**. El modo de depurador mejora el uso de un depurador del kernel de Microsoft Windows a través de un puerto serie virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




