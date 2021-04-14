---
description: Permite que un administrador administre las propiedades de cuota de disco de un volumen.
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
ms.openlocfilehash: 843f33ee79e70309a47f170bb1935f94f45c8f2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997817"
---
# <a name="diskquotacontrol-object"></a>Objeto DiskQuotaControl

Permite que un administrador administre las propiedades de cuota de disco de un volumen. El sistema de archivos NTFS permite que un administrador administre el uso de disco en un volumen compartido asignando una cantidad especificada de espacio en disco, o *límite de cuota*, a cada usuario. Puede utilizar este objeto para establecer el límite de cuota predeterminado que se asignará automáticamente a todos los nuevos usuarios.

## <a name="members"></a>Miembros

El objeto **DiskQuotaControl** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El objeto **DiskQuotaControl** tiene estos eventos.



| Evento                                                           | Descripción                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Se produce cuando se ha resuelto la información de nombre de un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) .<br/> |



 

### <a name="methods"></a>Métodos

El objeto **DiskQuotaControl** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Asigna una cuota de disco no predeterminada a un nuevo usuario.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Elimina un usuario del volumen.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Coloca el objeto de usuario especificado junto a la línea para la resolución de nombres.<br/>              |
| [**Inicialización**](diskquotacontrol-initialize.md)                                         | Abre un volumen especificado e inicializa su objeto de control de cuota.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Invalida la memoria caché de nombres de usuario del identificador de seguridad.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Cierra el subproceso de resolución de nombres de usuario.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Traduce un nombre de inicio de sesión al ID. de seguridad de usuario correspondiente en formato de cadena.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **DiskQuotaControl** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lectura/escritura<br/> | Establece u obtiene el límite de cuota predeterminado.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Solo lectura<br/>  | Obtiene el límite de cuota predeterminado como una cadena de texto.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lectura/escritura<br/> | Establece u obtiene el umbral de cuota predeterminado.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Solo lectura<br/>  | Obtiene el umbral de cuota predeterminado como una cadena de texto.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lectura/escritura<br/> | Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lectura/escritura<br/> | Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Solo lectura<br/>  | Obtiene un valor booleano que indica si se ha completado el archivo de cuota para el volumen.<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Solo lectura<br/>  | Obtiene un valor booleano que indica si el archivo de cuota para el volumen se está recompilando actualmente.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Lectura/escritura<br/> | Establece u obtiene el estado de las cuotas de disco del volumen.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lectura/escritura<br/> | Establece u obtiene un valor que controla cómo se resuelve el SID de usuario en los nombres de usuario.<br/>                                                                        |



 

## <a name="remarks"></a>Observaciones

Un administrador puede usar el objeto **DiskQuotaControl** para realizar varias tareas, entre las que se incluyen las siguientes:

-   Habilitar y deshabilitar el sistema de cuota de disco del volumen.
-   Obtención del estado del sistema de cuota en el volumen.
-   Denegando espacio en disco a los usuarios que superen su límite de cuota.
-   Especificar los valores predeterminados de umbral de advertencia y límite de cuota que se asignarán a los nuevos usuarios.
-   Agregar y quitar usuarios.

El objeto **DiskQuotaControl** permite establecer los valores predeterminados globales del volumen para propiedades como los límites de cuota. Sin embargo, cada usuario está representado por un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) que se puede usar para especificar la configuración de cuota individual.

Hay varias maneras de obtener el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) de un usuario:

-   Los objetos [**DIDiskQuotaUser**](didiskquotauser-object.md) para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar. Para obtener una explicación de cómo enumerar los objetos **DIDiskQuotaUser** , vea **Enumerating Disk quota users** en la sección Comentarios de **DIDiskQuotaUser**.
-   Al agregar un nuevo usuario, el método [**adduser**](diskquotacontrol-adduser.md) devuelve el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.
-   Si tiene el nombre del usuario, el método [**FindUser**](diskquotacontrol-finduser.md) devuelve el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.

Este objeto hace que la funcionalidad esencial de la interfaz IDiskQuotaControl esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de Shell**](shell.md)
</dt> </dl>

 

 




