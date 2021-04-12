---
title: MDM_Policy_User_Config01_Notifications02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Notifications02 representa las directivas de notificación disponibles.
ms.assetid: da70b3b4-e8ed-4784-ad6b-52e152a8b78f
keywords:
- MDM_Policy_User_Config01_Notifications02 (clase)
- MDM_Policy_User_Config01_Notifications02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Notifications02
- MDM_Policy_User_Config01_Notifications02.InstanceID
- MDM_Policy_User_Config01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c85dcd9a622d29baf6d7c8f28d9e72b68998ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150350"
---
# <a name="mdm_policy_user_config01_notifications02-class"></a>\_Clase Notifications02 de usuario de directiva MDM \_ \_ Config01 \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ Config01 de usuario de directiva de MDM \_ \_ \_ Notifications02** representa las directivas de notificación disponibles.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a>Miembros

La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Notifications02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Notifications02** tiene estas propiedades.

<dl> <dt>

[DisallowNotificationMirroring](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
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

Identifica el nombre del nodo primario. Para esta clase, la cadena es "notifications".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Config".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



 

