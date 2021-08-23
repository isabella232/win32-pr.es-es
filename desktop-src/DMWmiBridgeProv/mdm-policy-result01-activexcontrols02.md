---
title: MDM_Policy_Result01_ActiveXControls02 clase
description: La clase Mdm \_ Policy \_ Result01 \_ ActiveXControls02 representa las directivas de controles ActiveX MDM Policy.
ms.assetid: 46778743-59d7-4d37-836c-3f263bb8a083
keywords:
- MDM_Policy_Result01_ActiveXControls02 clase
- MDM_Policy_Result01_ActiveXControls02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ActiveXControls02
- MDM_Policy_Result01_ActiveXControls02.InstanceID
- MDM_Policy_Result01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ec2a78dc1271a71349fae1cc6e352eeb1086b0b74c07a209b2bbca0c9234b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077119"
---
# <a name="mdm_policy_result01_activexcontrols02-class"></a>Clase \_ \_ \_ ActiveXControls02 de Mdm Policy Result01

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La clase Mdm \_ Policy \_ Result01 \_ ActiveXControls02 representa las directivas de controles ActiveX MDM Policy.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a>Miembros

La **clase Mdm Policy \_ \_ Result01 \_ ActiveXControls02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Mdm Policy \_ \_ Result01 \_ ActiveXControls02** tiene estas propiedades.

<dl> <dt>

[ApprovedInstallationSites](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
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

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
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



 

