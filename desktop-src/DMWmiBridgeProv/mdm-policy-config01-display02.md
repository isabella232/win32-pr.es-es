---
title: MDM_Policy_Config01_Display02 (clase)
description: La \_ clase Config01 de Display02 de directivas MDM \_ \_ configura las directivas de visualización.
ms.assetid: 106eecc5-ede0-4d66-ba51-967a8f7bcb66
keywords:
- MDM_Policy_Config01_Display02 (clase)
- MDM_Policy_Config01_Display02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Display02
- MDM_Policy_Config01_Display02.InstanceID
- MDM_Policy_Config01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e79861a911d03f1d9174053dc8ec7c62824fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150106"
---
# <a name="mdm_policy_config01_display02-class"></a>\_ \_ Clase Display02 de Config01 de directivas MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La \_ clase Config01 de Display02 de directivas MDM \_ \_ configura las directivas de visualización.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a>Miembros

La clase Config01 de la **\_ Directiva MDM \_ \_ Display02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Config01 de \_ Display02 de directivas MDM** tiene estas propiedades.

<dl> <dt>

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

[TurnOffGdiDPIScalingForApps](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[TurnOnGdiDPIScalingForApps](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
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



 

