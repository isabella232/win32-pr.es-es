---
title: MDM_Policy_User_Result01_Start02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Start02 representa las directivas de inicio disponibles que se establecen por usuario.
ms.assetid: f7b63db4-f48d-44d2-b343-88cbc8f89cbe
keywords:
- MDM_Policy_User_Result01_Start02 (clase)
- MDM_Policy_User_Result01_Start02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Start02
- MDM_Policy_User_Result01_Start02.InstanceID
- MDM_Policy_User_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6765a693ef9b4fc579a1bfc5f869db236003801
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489185"
---
# <a name="mdm_policy_user_result01_start02-class"></a>\_Clase Start02 de usuario de directiva MDM \_ \_ Result01 \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ Result01 de usuario de directiva de MDM \_ \_ \_ Start02** representa las directivas de inicio disponibles que se establecen por usuario.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a>Miembros

La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Start02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Start02** tiene estas propiedades.

<dl> <dt>

[HidePeopleBar](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
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

Identifica el nombre del nodo primario. Para esta clase, la cadena es "Start".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Result".

</dd> <dt>

[StartLayout](/windows/client-management/mdm/policy-csp-start#start-startlayout)
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

