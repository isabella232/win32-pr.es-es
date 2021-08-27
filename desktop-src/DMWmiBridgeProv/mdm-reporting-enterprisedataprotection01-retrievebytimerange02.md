---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 clase
description: La clase Mdm \_ Reporting \_ EnterpriseDataProtection01 RetrieveByTimeRange02 se usa para recuperar los registros que existen dentro de \_ StartTime y StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 clase
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60952e10f437b75edb4edf5a9465d4926b7e0615cc736f19f31520e02997d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045615"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a>Mdm \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 (clase)

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** se usa para recuperar los registros que existen dentro de StartTime y StopTime. StartTime y StopTime se expresan en formato ISO 8601. Si no se especifican StartTime y StopTime, los valores se interpretan como la primera hora existente o la última existente.

Estos son los otros escenarios posibles:

-   Si no se especifican StartTime y StopTime, devuelve todos los registros existentes.
-   Si se especifica StopTime, pero no se especifica StartTime, se devuelven todos los registros que existen antes de StopTime.
-   Si se especifica StartTime, pero no se especifica StopTime, se devuelven todos los registros que existen desde StartTime.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a>Miembros

La **clase Mdm \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es "RetrieveByTimeRange".

</dd> <dt>

[Registros](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseDataProtection".

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[Tipo](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 

