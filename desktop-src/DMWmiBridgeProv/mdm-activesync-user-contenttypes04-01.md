---
title: MDM_ActiveSync_User_ContentTypes04_01 (clase)
description: La \_ \_ \_ clase ContentTypes04 01 de usuario \_ de MDM define el tipo de contenido que se va a habilitar o deshabilitar individualmente para la sincronización.
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- MDM_ActiveSync_User_ContentTypes04_01 (clase)
- MDM_ActiveSync_User_ContentTypes04_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656524"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a>\_ \_ \_ Clase ContentTypes04 01 de \_ usuario de MDM ActiveSync

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ \_ \_ ContentTypes04 \_ 01 de usuario de MDM** define el tipo de contenido que se va a habilitar o deshabilitar individualmente para la sincronización.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ \_ ContentTypes04 \_ 01 de usuario de MDM ActiveSync** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ \_ ContentTypes04 \_ 01 de usuario de MDM ActiveSync** tiene estas propiedades.

<dl> <dt>

[Enabled](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
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

Identifica el nombre del nodo primario.

</dd> <dt>

[Nombre](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options".

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

 

