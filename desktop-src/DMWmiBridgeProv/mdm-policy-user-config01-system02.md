---
title: MDM_Policy_User_Config01_System02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ System02 representa las directivas de telemetría disponibles.
ms.assetid: 3f049152-6868-4b10-8711-dadc4cb012b4
keywords:
- MDM_Policy_User_Config01_System02 (clase)
- MDM_Policy_User_Config01_System02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_System02
- MDM_Policy_User_Config01_System02.InstanceID
- MDM_Policy_User_Config01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eefa8a08320b79c80d4e0cb359fd1194a21ae4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150346"
---
# <a name="mdm_policy_user_config01_system02-class"></a>\_Clase System02 de usuario de directiva MDM \_ \_ Config01 \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ System02 representa las directivas de telemetría disponibles.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTelemetry;
};
```

## <a name="members"></a>Miembros

La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ System02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ System02** tiene estas propiedades.

<dl> <dt>

[AllowTelemetry](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
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

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
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



 

