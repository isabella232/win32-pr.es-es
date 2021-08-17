---
description: Proporciona información adicional que se usará con el método ExportReferencePoint de la clase Msvm \_ VirtualSystemReferencePointService.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Msvm_VirtualSystemReferencePointExportSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b3fc743d8431d76582553979bb25e1269df970d70187c65c2bddd1014834c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147948"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>Clase Msvm \_ VirtualSystemReferencePointExportSettingData

Proporciona información adicional que se usará con el [**método ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) de la clase [**Msvm \_ VirtualSystemReferencePointService.**](msvm-virtualsystemreferencepointservice.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualSystemReferencePointExportSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemReferencePointExportSettingData** tiene estas propiedades.

<dl> <dt>

**BaseReferencePoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del punto de referencia base con respecto a la exportación que se debe realizar.

</dd> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Tipo de datos: **Matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los iDs de instancia wmi de los discos para los que se deben exportar los datos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




