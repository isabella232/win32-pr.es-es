---
description: Permite a un administrador administrar las propiedades de cuota de disco de un volumen.
title: Objeto DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579612"
---
# <a name="diskquotacontrol-object"></a>Objeto DiskQuotaControl

Permite a un administrador administrar las propiedades de cuota de disco de un volumen. El sistema de archivos NTFS permite a un administrador administrar el uso del disco en un volumen compartido mediante la asignación de una cantidad especificada de espacio en disco, o límite de *cuota,* a cada usuario. Puede usar este objeto para establecer el límite de cuota predeterminado que se asignará automáticamente a todos los usuarios nuevos.

## <a name="members"></a>Members

El **objeto DiskQuotaControl** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El **objeto DiskQuotaControl** tiene estos eventos.



| Evento                                                           | Descripción                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Se produce cuando se ha resuelto la información de nombre de un objeto [**DIDiskQuotaUser.**](didiskquotauser-object.md)<br/> |



 

### <a name="methods"></a>Métodos

El **objeto DiskQuotaControl** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Asigna una cuota de disco no predeterminada a un nuevo usuario.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Elimina un usuario del volumen.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Coloca el objeto de usuario especificado a continuación en línea para la resolución de nombres.<br/>              |
| [**Inicialización**](diskquotacontrol-initialize.md)                                         | Abre un volumen especificado e inicializa su objeto de control de cuota.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Invalida la caché de nombres de usuario del identificador de seguridad.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Apaga el subproceso de resolución de nombres de usuario.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Traduce un nombre de inicio de sesión al identificador de seguridad de usuario correspondiente en formato de cadena.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto DiskQuotaControl** tiene estas propiedades.



| Propiedad.                                                                                   | Tipo de acceso           | Descripción                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lectura y escritura<br/> | Establece u obtiene el límite de cuota predeterminado.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Solo lectura<br/>  | Obtiene el límite de cuota predeterminado como una cadena de texto.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lectura y escritura<br/> | Establece u obtiene el umbral de cuota predeterminado.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Solo lectura<br/>  | Obtiene el umbral de cuota predeterminado como una cadena de texto.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lectura y escritura<br/> | Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lectura y escritura<br/> | Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Solo lectura<br/>  | Obtiene un valor booleano que indica si el archivo de cuota del volumen está completo.<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Solo lectura<br/>  | Obtiene un valor booleano que indica si el archivo de cuota del volumen se está recompilando actualmente.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Lectura y escritura<br/> | Establece u obtiene el estado de las cuotas de disco del volumen.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lectura y escritura<br/> | Establece u obtiene un valor que controla cómo se resuelve el SID de usuario en los nombres de usuario.<br/>                                                                        |



 

## <a name="remarks"></a>Observaciones

Un administrador puede usar el **objeto DiskQuotaControl** para realizar una serie de tareas, incluidas las siguientes:

-   Habilitación y deshabilitación del sistema de cuota de disco del volumen.
-   Obtener el estado del sistema de cuota en el volumen.
-   Denegar espacio en disco a los usuarios que superen su límite de cuota.
-   Especificar los valores predeterminados de umbral de advertencia y límite de cuota que se asignarán a los nuevos usuarios.
-   Agregar y quitar usuarios.

El **objeto DiskQuotaControl** permite establecer valores predeterminados globales para el volumen para propiedades como límites de cuota. Sin embargo, cada usuario se representa mediante un [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) que se puede usar para especificar la configuración de cuota individual.

Hay varias maneras de obtener el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) de un usuario:

-   Los [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar. Para obtener una explicación sobre cómo enumerar objetos **DIDiskQuotaUser,** vea **Enumerating Disk Quota Users (Enumeración** de usuarios de cuota de disco) en la sección Comentarios de **DIDiskQuotaUser**.
-   Al agregar un nuevo usuario, el [**método AddUser**](diskquotacontrol-adduser.md) devuelve el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.
-   Si tiene el nombre del usuario, el [**método FindUser**](diskquotacontrol-finduser.md) devuelve el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.

Este objeto hace que la funcionalidad esencial de la interfaz IDiskQuotaControl esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Shell**](shell.md)
</dt> </dl>

 

 




