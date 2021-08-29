---
title: MDM_Policy_Result01_AboveLock02 clase
description: La clase MDM \_ Policy \_ Result01 AboveLock02 representa las directivas que determinan las acciones permitidas por encima \_ de la pantalla Bloqueo de dispositivo.
ms.assetid: 0b6d4083-2484-450b-9261-5ef339db4707
keywords:
- MDM_Policy_Result01_AboveLock02 clase
- MDM_Policy_Result01_AboveLock02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AboveLock02
- MDM_Policy_Result01_AboveLock02.InstanceID
- MDM_Policy_Result01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a87dfe1c3c36e3728de797dbebb889938c197d3bbc0e84c5e181b556659f86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077129"
---
# <a name="mdm_policy_result01_abovelock02-class"></a>Clase Mdm \_ Policy \_ Result01 \_ AboveLock02

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM Policy \_ \_ Result01 \_ AboveLock02** representa las directivas que determinan las acciones que se permiten encima de la pantalla Bloqueo de dispositivo.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a>Miembros

La **clase MDM Policy \_ \_ Result01 \_ AboveLock02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MDM Policy \_ \_ Result01 \_ AboveLock02** tiene estas propiedades.

<dl> <dt>

[AllowCortanaAboveLock](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[AllowToasts](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
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

Identifica el nombre del nodo primario. Para esta clase, la cadena es "AboveLock".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | DMMap \\ de MDM de CIMv2 \\ \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

