---
title: TaskService. Connect (método)
description: Para el scripting, se conecta a un equipo remoto y asocia todas las llamadas subsiguientes en esta interfaz a una sesión remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Método Connect Programador de tareas
- Método Connect Programador de tareas, objeto TaskService
- Programador de tareas de objeto TaskService, método Connect
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
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996155"
---
# <a name="taskserviceconnect-method"></a>TaskService. Connect (método)

Para el scripting, se conecta a un equipo remoto y asocia todas las llamadas subsiguientes en esta interfaz a una sesión remota. Si el parámetro serverName está vacío, este método se ejecutará en el equipo local. Si no se especifica userId, se usa el token actual.

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

*nombreDeServidor* \[ en, opcional\]
</dt> <dd>

Nombre del equipo al que desea conectarse. Si el parámetro serverName está vacío, este método se ejecutará en el equipo local.

</dd> <dt>

*usuario* \[ de en, opcional\]
</dt> <dd>

El nombre de usuario que se usa durante la conexión al equipo. Si no se especifica el usuario, se usa el token actual.

</dd> <dt>

*dominio* \[ de en, opcional\]
</dt> <dd>

Dominio del usuario especificado en el parámetro de *usuario* .

</dd> <dt>

*contraseña* \[ de en, opcional\]
</dt> <dd>

La contraseña que se utiliza para conectarse al equipo. Si no se especifican el nombre de usuario y la contraseña, se usa el token actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe llamar al método **TaskService. Connect** antes de llamar a cualquiera de los otros métodos [**TaskService**](taskservice.md) .

Si se produce un error en el método Connect, puede recopilar el identificador de error para encontrar el significado del error. En la tabla siguiente se enumeran los identificadores de error y sus descripciones.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificador de error</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>Se denegó el acceso para conectarse al servicio de Programador de tareas.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>El servicio Programador de tareas no se está ejecutando.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>La aplicación no tiene suficiente memoria para completar la operación o el <em>usuario</em>, la <em>contraseña</em>o el <em>dominio</em> tiene al menos un valor NULL y un valor distinto de NULL.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Este error se devuelve en las situaciones siguientes:
<ul>
<li>El nombre de equipo especificado en el parámetro <em>ServerName</em> no existe.</li>
<li>Cuando intenta conectarse a un equipo con Windows Server 2003 o Windows XP, y el equipo remoto no tiene la excepción de Firewall compartir archivos e impresoras habilitada o el servicio de registro remoto no se está ejecutando.</li>
<li>Cuando intenta conectarse a un equipo con Windows Vista, y el equipo remoto no tiene habilitada la excepción del firewall administración remota de tareas programadas y la excepción de Firewall compartir archivos e impresoras está habilitada, o el servicio registro remoto no se está ejecutando.</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>Los parámetros <em>User</em>, <em>password</em>o <em>Domain</em> no se pueden especificar al conectarse a un equipo remoto con Windows XP o Windows Server 2003 desde un equipo con Windows Vista.</td>
</tr>
</tbody>
</table>



 

Si va a conectarse a un equipo remoto de Windows Vista desde Windows Vista, debe permitir la excepción del firewall administración remota de tareas programadas en el equipo remoto. Para permitir esta excepción, haga clic en Inicio, Panel de control, Seguridad, Dejar pasar a un programa a través de Firewall de Windows y, a continuación, active la casilla Administración remota de tareas programadas. A continuación, haga clic en el botón Aceptar en el cuadro de diálogo Configuración de Firewall de Windows.

Si va a conectarse a un equipo remoto equipado con Windows XP o Windows Server 2003 desde un equipo equipado con Windows Vista, necesita permitir la excepción de firewall Compartir archivos e impresoras en el equipo remoto. Para permitir esta excepción, haga clic en Inicio, Panel de control, haga doble clic en Firewall de Windows, seleccione la ficha Excepciones y, a continuación, seleccione la excepción de firewall Compartir archivos e impresoras. A continuación, haga clic en el botón Aceptar del cuadro de diálogo Firewall de Windows. El servicio de registro remoto también debe estar en ejecución en el equipo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





