---
title: MDM_ActiveSync_User_Options03 (clase)
description: La \_ \_ clase Options03 de usuario de MDM ActiveSync \_ define las opciones que se establecen para cada cuenta de ActiveSync.
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- MDM_ActiveSync_User_Options03 (clase)
- MDM_ActiveSync_User_Options03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150182"
---
# <a name="mdm_activesync_user_options03-class"></a>\_ \_ Clase Options03 de usuario de MDM ActiveSync \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ \_ \_ Options03 de usuario de MDM ActiveSync** define las opciones que se establecen para cada cuenta de ActiveSync.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ \_ Options03 de usuario de MDM ActiveSync** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ \_ Options03 de usuario de MDM ActiveSync** tiene estas propiedades.

<dl> <dt>

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

[Logging](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[MailAgeFilter](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"

</dd> <dt>

[Programación](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[UseSSL](/windows/client-management/mdm/activesync-csp#options-usessl)
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

 

