---
title: MDM_Policy_User_Result01_AttachmentManager02 clase
description: La clase Mdm \_ Policy \_ User \_ Result01 \_ AttachmentManager02 representa las directivas de administrador de datos adjuntos disponibles.
ms.assetid: c6cfec0d-24f8-4356-a12b-d9b9944776a7
keywords:
- MDM_Policy_User_Result01_AttachmentManager02 clase
- MDM_Policy_User_Result01_AttachmentManager02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02.InstanceID
- MDM_Policy_User_Result01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d646a58cb2d8cd3330ca7f182f7b3213fe0f76479ecd94bd0a13e9d19794b163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750415"
---
# <a name="mdm_policy_user_result01_attachmentmanager02-class"></a>Mdm \_ Policy \_ User \_ Result01 \_ AttachmentManager02 (clase)

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La clase Mdm \_ Policy \_ User \_ Result01 \_ AttachmentManager02 representa las directivas de administrador de datos adjuntos disponibles.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a>Miembros

La **clase Mdm Policy User \_ \_ \_ Result01 \_ AttachmentManager02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Mdm Policy User \_ \_ \_ Result01 \_ AttachmentManager02** tiene estas propiedades.

<dl> <dt>

[DoNotPreserveZoneInformation](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[HideZoneInfoMechanism](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
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

[NotifyAntivirusPrograms](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
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



 

