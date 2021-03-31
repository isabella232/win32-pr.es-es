---
title: MDM_Policy_Config01_Autoplay02 (clase)
description: La \_ clase Config01 de Autoplay02 de directivas MDM \_ \_ configura las directivas de reproducción automática disponibles.
ms.assetid: ef7ccdb6-3f77-4c43-87d9-56acda97be21
keywords:
- MDM_Policy_Config01_Autoplay02 (clase)
- MDM_Policy_Config01_Autoplay02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Autoplay02
- MDM_Policy_Config01_Autoplay02.InstanceID
- MDM_Policy_Config01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e064d0b0eed457bcafdf4da9bf8e72fbb4916e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079182"
---
# <a name="mdm_policy_config01_autoplay02-class"></a>\_ \_ Clase Autoplay02 de Config01 de directivas MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La \_ clase Config01 de Autoplay02 de directivas MDM \_ \_ configura las directivas de reproducción automática disponibles.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a>Miembros

La clase Config01 de la **\_ Directiva MDM \_ \_ Autoplay02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Config01 de \_ Autoplay02 de directivas MDM** tiene estas propiedades.

<dl> <dt>

[DisallowAutoplayForNonVolumeDevices](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
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

</dd> <dt>

[SetDefaultAutoRunBehavior](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[TurnOffAutoPlay](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

