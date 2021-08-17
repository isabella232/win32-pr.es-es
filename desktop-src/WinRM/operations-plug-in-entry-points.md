---
title: Puntos de entrada del complemento de operaciones
description: Puntos de entrada del complemento de operaciones
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5941746e8e6b952f2f1cd6f21c697398cb4cbb60b024daa557e65151a0a1cfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412775"
---
# <a name="operations-plug-in-entry-points"></a>Puntos de entrada del complemento de operaciones

Un complemento de operaciones debe implementar determinados puntos de entrada en función de las funcionalidades que quiera admitir.

Un complemento debe registrarse con el servicio Windows Remote Management (WinRM), que contiene los nombres de los puntos de entrada dll del complemento. Todas las operaciones tienen puntos de entrada DLL predefinidos que deben exponerse si se admite esa operación.

En la tabla siguiente se proporciona información general sobre los puntos de entrada del complemento de operaciones en la API del complemento WinRM.



| Función                                                                                 | Descripción                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMANDO DEL COMPLEMENTO WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Define la devolución de llamada de comando para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command).<br/> |
| [**WSMAN \_ PLUGIN \_ CONNECT**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Define la devolución de llamada de conexión para un complemento.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginConnect.**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)<br/>                                                                                                |
| [**RECEPCIÓN DEL COMPLEMENTO WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Define la devolución de llamada de recepción para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginReceive.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)<br/> |
| [**CONTEXTO DEL COMANDO \_ RELEASE \_ DEL COMPLEMENTO \_ \_ WSMAN**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Define la devolución de llamada del comando release para el complemento.<br/> El nombre del punto de entrada dll debe [**ser WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                        |
| [**CONTEXTO DEL \_ SHELL DE VERSIÓN DEL \_ COMPLEMENTO \_ WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Define la devolución de llamada del shell de versión para el complemento.<br/> El nombre del punto de entrada dll debe [**ser WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                          |
| [**ENVÍO DEL COMPLEMENTO WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Define la devolución de llamada de envío para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginSend.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)<br/>          |
| [**SHELL DEL COMPLEMENTO WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Define la devolución de llamada del shell para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell).<br/>       |
| [**APAGADO DEL COMPLEMENTO WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Define la devolución de llamada de apagado del complemento.<br/> Todos los complementos de WinRM deben implementar esta función de devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown).<br/>                      |
| [**WSMAN \_ PLUGIN \_ SIGNAL**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Define la devolución de llamada de señal para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginSignal.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)<br/>    |
| [**INICIO DEL COMPLEMENTO WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Define la devolución de llamada de inicio para el complemento.<br/> Todos los complementos de WinRM deben implementar esta función de devolución de llamada.<br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginStartup.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)<br/>                         |



 

 

