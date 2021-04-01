---
description: Explica las entradas del registro para los eventos de Winlogon.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Entradas del registro (autenticación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d50b413d99d2bc31a7af4e8e101ab27e51a8892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909406"
---
# <a name="registry-entries-authentication"></a>Entradas del registro (autenticación)

Para que el paquete reciba notificaciones de eventos de [*Winlogon*](../secgloss/w-gly.md), debe proporcionar el nombre del paquete, los nombres de las funciones del controlador de eventos en el paquete, el archivo dll responsable de implementar el paquete e información sobre si el archivo dll admite eventos asincrónicos y suplantación.

Debe crear la clave del registro del paquete de notificación como una subclave de

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Notify**

El nombre de la clave suele ser el mismo que el nombre del archivo DLL; sin embargo, esto no es obligatorio. El nombre elegido para el paquete no debe entrar en conflicto con los nombres de otros paquetes de notificación instalados.

En la clave **Notify** del registro, cree los siguientes valores del registro si hay una función de controlador de eventos pertinente en el paquete.



| Tipo de datos de nombre de valor \[\]                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Asincrónica** \[ **Reg \_ . DWORD**\]<br/>    | Indica si el paquete puede controlar los eventos de forma asincrónica. Si este valor se establece en 1, Winlogon llama a las funciones del paquete en un subproceso independiente. De lo contrario, no la tiene.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **Reg \_ . EXPANDIR \_ SZ**\]<br/>    | Nombre del archivo DLL que implementa el paquete de notificación, por ejemplo: "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| **Suplantar** \[ **Reg \_ . DWORD**\]<br/>     | Indica si Winlogon debe suplantar el [*contexto*](../secgloss/c-gly.md) de seguridad del usuario que ha iniciado sesión cuando llama a las funciones del paquete de notificación. Si este valor se establece en 1, Winlogon utiliza la suplantación. De lo contrario, no la tiene.<br/>                                                                                                                    |
| **Bloquear** \[ **Reg \_ . SZ**\]<br/>               | Nombre de la función que controla los eventos de bloqueo del escritorio, por ejemplo: "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
| **Cerrar sesión** \[ **Reg \_ . SZ**\]<br/>             | Nombre de la función que controla los eventos de cierre de sesión, por ejemplo: "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Inicio de sesión** \[ **Reg \_ . SZ**\]<br/>              | Nombre de la función que controla los eventos de inicio de sesión, por ejemplo: "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Apagar** \[ **Reg \_ . SZ**\]<br/>           | Nombre de la función que controla los eventos de cierre, por ejemplo: "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **DWORD**\]<br/> | Indica si Winlogon debe generar una notificación para los eventos de inicio de sesión de tarjetas inteligentes. Si este valor se establece en 1, Winlogon permite las notificaciones de tarjeta inteligente. De lo contrario, no la tiene.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **Reg \_ . SZ**\]<br/>   | Nombre de la función que controla los eventos de inicio del protector de pantalla, por ejemplo: "WLEventStartScreenSaver".<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **Reg \_ . SZ**\]<br/>         | Nombre de la función que controla los eventos de inicio del shell, por ejemplo: "WLEventStartShell".<br/> Un evento de inicio de Shell se produce después de que el usuario haya iniciado sesión, pero antes de que aparezca el escritorio. Difiere del evento Logon en que se ha establecido el [*contexto*](../secgloss/c-gly.md) de seguridad del usuario y se encuentran disponibles recursos como las conexiones de red.<br/> |
| **Inicio** \[ de **Reg \_ . SZ**\]<br/>            | Nombre de la función que controla los eventos de inicio del sistema, por ejemplo: "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **Reg \_ . SZ**\]<br/>    | Nombre de la función que controla los eventos de detención del protector de pantalla, por ejemplo: "WLEventStopScreenSaver".<br/>                                                                                                                                                                                                                                                                                                            |
| **Desbloquear** \[ **Reg \_ . SZ**\]<br/>             | Nombre de la función que controla los eventos de desbloqueo del escritorio, por ejemplo: "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
