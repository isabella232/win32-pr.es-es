---
description: Explica las entradas del Registro para los eventos winlogon.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Entradas del Registro (autenticación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d50b413d99d2bc31a7af4e8e101ab27e51a8892
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259668"
---
# <a name="registry-entries-authentication"></a>Entradas del Registro (autenticación)

Para que el paquete reciba notificaciones de eventos de [*Winlogon,*](../secgloss/w-gly.md)debe proporcionar el nombre del paquete, los nombres de las funciones del controlador de eventos en el paquete, el archivo DLL responsable de implementar el paquete e información sobre si el archivo DLL admite eventos asincrónicos y suplantación.

Debe crear la clave del Registro del paquete de notificación como una subclave de

**HKEY \_ Notificación \_ de** \\  \\  \\  \\  \\ **Winlogon** \\  de Microsoft Windows NT CurrentVersion Software LOCAL MACHINE

El nombre de la clave suele ser el mismo que el nombre del archivo DLL; sin embargo, esto no es obligatorio. El nombre elegido para el paquete no debe estar en conflicto con los nombres de otros paquetes de notificación instalados.

En la clave del Registro **Notify,** cree los siguientes valores del Registro si hay una función de controlador de eventos pertinente en el paquete.



| Tipo de datos de \[ nombre de valor\]                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Asincrónico** \[ **REG \_ DWORD**\]<br/>    | Indica si el paquete puede controlar eventos de forma asincrónica. Si este valor se establece en 1, Winlogon llama a las funciones de paquete en un subproceso independiente. De lo contrario, no la tiene.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **REG \_ EXPANDIR \_ SZ**\]<br/>    | Nombre del archivo DLL que implementa el paquete de notificación, por ejemplo: "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| **Suplantar** \[ **REG \_ DWORD**\]<br/>     | Indica si Winlogon debe suplantar el contexto de seguridad del usuario que inició sesión cuando llama a las funciones del paquete de notificación. [](../secgloss/c-gly.md) Si este valor se establece en 1, Winlogon usa la suplantación. De lo contrario, no la tiene.<br/>                                                                                                                    |
| **Bloqueo** \[ **REG \_ SZ**\]<br/>               | Nombre de la función que controla eventos de bloqueo de escritorio, por ejemplo: "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
| **Cierre de sesión** \[ **REG \_ SZ**\]<br/>             | Nombre de la función que controla los eventos de cierre de sesión, por ejemplo: "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Inicio de sesión** \[ **REG \_ SZ**\]<br/>              | Nombre de la función que controla los eventos de inicio de sesión, por ejemplo: "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Apagado** \[ **REG \_ SZ**\]<br/>           | Nombre de la función que controla los eventos de apagado, por ejemplo: "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **DWORD**\]<br/> | Indica si Winlogon debe generar una notificación para los eventos de inicio de sesión a partir de tarjetas inteligentes. Si este valor se establece en 1, Winlogon permite notificaciones de tarjeta inteligente. De lo contrario, no la tiene.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **REG \_ SZ**\]<br/>   | Nombre de la función que controla los eventos de inicio del protector de pantalla, por ejemplo: "WLEventStartScreenSaver".<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **REG \_ SZ**\]<br/>         | Nombre de la función que controla los eventos de inicio del shell, por ejemplo: "WLEventStartShell".<br/> Un evento de inicio del shell se produce después de que el usuario haya iniciado sesión, pero antes de que aparezca el escritorio. Difiere del evento de inicio de sesión [](../secgloss/c-gly.md) en que se ha establecido el contexto de seguridad del usuario y hay recursos disponibles, como las conexiones de red.<br/> |
| **Inicio** \[ **REG \_ SZ**\]<br/>            | Nombre de la función que controla los eventos de inicio del sistema, por ejemplo: "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **REG \_ SZ**\]<br/>    | Nombre de la función que controla los eventos de detención del protector de pantalla, por ejemplo: "WLEventStopScreenSaver".<br/>                                                                                                                                                                                                                                                                                                            |
| **Desbloqueo** \[ **REG \_ SZ**\]<br/>             | Nombre de la función que controla eventos de desbloqueo de escritorio, por ejemplo: "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
