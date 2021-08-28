---
description: Proporciona información adicional que se usará con el método CreateReferencePoint de la clase \_ CollectionReferencePointService de Msvm.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Msvm_CollectionReferencePointSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1164c61f9335ce900dfbcf0b317dd0c4c9a8f84c0a97aaf13b2ea851a80dbd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130675"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a>Clase \_ CollectionReferencePointSettingData de Msvm

Proporciona información adicional que se usará con el [**método CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) de la clase [**\_ CollectionReferencePointService de Msvm.**](msvm-collectionreferencepointservice.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Miembros

La **clase \_ CollectionReferencePointSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ CollectionReferencePointSettingData** tiene estas propiedades.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nivel de coherencia del punto de referencia.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente con la** aplicación (1)


</dt> <dd>

El punto de referencia indica un momento dado en el tiempo en el que el sistema virtual estaba en estado coherente con los bloqueos.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherente con bloqueos** (2)


</dt> <dd>

El punto de referencia indica un momento dado en el tiempo en el que el sistema virtual estaba en estado coherente con la aplicación.

</dd> </dl>

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

 

 




