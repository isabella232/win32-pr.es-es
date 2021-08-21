---
title: MDM_Policy_Config01_SmartScreen02 clase
description: La clase MDM \_ Policy \_ Config01 \_ SmartScreen02 configura las directivas de pantalla inteligente.
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- MDM_Policy_Config01_SmartScreen02 clase
- MDM_Policy_Config01_SmartScreen02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49624cd014c71a1f459530cc889733a945d92603b0a539fce6c496988e302dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017823"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a>Clase Mdm \_ Policy \_ Config01 \_ SmartScreen02

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La clase MDM \_ Policy \_ Config01 \_ SmartScreen02 configura las directivas de pantalla inteligente.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a>Miembros

La **clase Mdm Policy \_ \_ Config01 \_ SmartScreen02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Mdm Policy \_ \_ Config01 \_ SmartScreen02** tiene estas propiedades.

<dl> <dt>

[EnableAppInstallControl](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[EnableSmartScreenInShell](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
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

[PreventOverrideForFilesInShell](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

