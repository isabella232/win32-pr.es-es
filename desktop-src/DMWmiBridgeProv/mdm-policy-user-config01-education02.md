---
title: MDM_Policy_User_Config01_Education02 clase
description: La clase \_ \_ \_ Config01 Education02 del usuario de directiva \_ MDM configura las directivas educativas.
ms.assetid: d9a263c7-ee9c-4857-b9a6-f0efdb373e13
keywords:
- MDM_Policy_User_Config01_Education02 clase
- MDM_Policy_User_Config01_Education02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02.InstanceID
- MDM_Policy_User_Config01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d004ca4dc440f21204d1eb6fdc6ba42169b623efa6b15ea823e1c7cadedcac0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694125"
---
# <a name="mdm_policy_user_config01_education02-class"></a>Clase Mdm \_ Policy \_ User \_ Config01 \_ Education02

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La clase \_ \_ \_ Config01 Education02 del usuario de directiva \_ MDM configura las directivas educativas.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a>Miembros

La **clase Mdm Policy User \_ \_ \_ Config01 \_ Education02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Mdm Policy User \_ \_ \_ Config01 \_ Education02** tiene estas propiedades.

<dl> <dt>

[DefaultPrinterName](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
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

[PreventAddingNewPrinters](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[PrinterNames](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

