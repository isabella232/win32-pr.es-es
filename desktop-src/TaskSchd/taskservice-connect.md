---
title: TaskService. Conectar método
description: Para el scripting, se conecta a un equipo remoto y asocia todas las llamadas posteriores en esta interfaz a una sesión remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Conectar método Programador de tareas
- Conectar método Programador de tareas , objeto TaskService
- TaskService object Programador de tareas , Conectar method
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8d9491fb66d8e79b18efed363d4eb4f21bc6c5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472351"
---
# <a name="taskserviceconnect-method"></a>TaskService. Conectar método

Para el scripting, se conecta a un equipo remoto y asocia todas las llamadas posteriores en esta interfaz a una sesión remota. Si el parámetro serverName está vacío, este método se ejecutará en el equipo local. Si no se especifica userId, se usa el token actual.

## <a name="syntax"></a>Sintaxis


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*serverName* \[ en, opcional\]
</dt> <dd>

Nombre del equipo al que desea conectarse. Si el parámetro serverName está vacío, este método se ejecutará en el equipo local.

</dd> <dt>

*usuario* \[ en, opcional\]
</dt> <dd>

Nombre de usuario que se usa durante la conexión al equipo. Si no se especifica el usuario, se usa el token actual.

</dd> <dt>

*dominio* \[ en, opcional\]
</dt> <dd>

Dominio del usuario especificado en el *parámetro de* usuario.

</dd> <dt>

*contraseña* \[ en, opcional\]
</dt> <dd>

Contraseña que se usa para conectarse al equipo. Si no se especifican el nombre de usuario y la contraseña, se usa el token actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se **debe llamar al Conectar TaskService.Conectar** antes de llamar a cualquiera de los otros [**métodos TaskService.**](taskservice.md)

Si se produce Conectar error en el método , puede recopilar el identificador de error para encontrar el significado del error. En la tabla siguiente se enumeran los identificadores de error y sus descripciones.




| Identificador de error | Descripción | 
|------------------|-------------|
| 0x80070005 | Se deniega el acceso para conectarse al Programador de tareas servicio. | 
| 0x80041315 | El Programador de tareas no se está ejecutando. | 
| 0x8007000e | La aplicación no tiene suficiente memoria para completar <em></em>la <em></em> operación o el usuario <em>,</em>la contraseña o el dominio tienen al menos un valor NULL y un valor distinto de NULL. | 
| 53 | Este error se devuelve en las situaciones siguientes:<ul><li>El nombre de equipo especificado en el <em>parámetro serverName</em> no existe.</li><li>Cuando intenta conectarse a un equipo de Windows Server 2003 o Windows XP, y el equipo remoto no tiene habilitada la excepción de firewall Uso compartido de archivos e impresoras o el servicio Registro remoto no se está ejecutando.</li><li>Cuando intenta conectarse a un equipo de Windows Vista, y el equipo remoto no tiene habilitada la excepción de firewall Administración de tareas programadas remotas y la excepción de firewall Uso compartido de archivos e impresoras habilitada, o el servicio Registro remoto no se está ejecutando.</li></ul> | 
| 50 | Los <em>parámetros</em> <em>de</em> <em></em> usuario , contraseña o dominio no se pueden especificar al conectarse a un equipo Windows XP o Windows Server 2003 desde un equipo Windows Vista. | 




 

Si va a conectarse a un equipo remoto de Windows Vista desde un Windows Vista, debe permitir la excepción de firewall Administración remota de tareas programadas en el equipo remoto. Para permitir esta excepción, haga clic en Inicio, Panel de control, Seguridad, Dejar pasar a un programa a través de Firewall de Windows y, a continuación, active la casilla Administración remota de tareas programadas. A continuación, haga clic en el botón Aceptar en el cuadro de diálogo Configuración de Firewall de Windows.

Si va a conectarse a un equipo remoto equipado con Windows XP o Windows Server 2003 desde un equipo equipado con Windows Vista, necesita permitir la excepción de firewall Compartir archivos e impresoras en el equipo remoto. Para permitir esta excepción, haga clic en Inicio, Panel de control, haga doble clic en Firewall de Windows, seleccione la ficha Excepciones y, a continuación, seleccione la excepción de firewall Compartir archivos e impresoras. A continuación, haga clic en el botón Aceptar en el Windows de diálogo Firewall. El servicio registro remoto también debe ejecutarse en el equipo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





