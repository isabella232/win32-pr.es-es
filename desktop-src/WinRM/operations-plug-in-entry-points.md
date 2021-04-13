---
title: Puntos de entrada del complemento de operaciones
description: Puntos de entrada del complemento de operaciones
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0834363c7447bc50269da09d361e630d9bc0615a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487735"
---
# <a name="operations-plug-in-entry-points"></a>Puntos de entrada del complemento de operaciones

Un complemento de operaciones debe implementar determinados puntos de entrada en función de las capacidades que desee admitir.

Un complemento debe registrarse con el servicio Administración remota de Windows (WinRM), que contiene los nombres de los puntos de entrada del archivo DLL del complemento. Todas las operaciones tienen puntos de entrada de DLL predefinidos que deben exponerse si se admite esa operación.

En la tabla siguiente se proporciona información general sobre los puntos de entrada del complemento de operaciones en la API del complemento WinRM.



| Función                                                                                 | Descripción                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_comando de complemento WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Define la devolución de llamada del comando para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de Shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command).<br/> |
| [**\_conexión de complemento WSMAN \_**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Define la devolución de llamada de conexión para un complemento.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginConnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect).<br/>                                                                                                |
| [**\_recepción del complemento WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Define la devolución de llamada de recepción para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de Shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginReceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive).<br/> |
| [**\_contexto de \_ comando de versión del complemento WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Define la devolución de llamada del comando RELEASE para el complemento.<br/> El nombre del punto de entrada del archivo DLL debe ser [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                        |
| [**\_contexto de \_ Shell de versión del complemento WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Define la devolución de llamada del shell de versión para el complemento.<br/> El nombre del punto de entrada del archivo DLL debe ser [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                          |
| [**\_envío del complemento WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Define la devolución de llamada de envío para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de Shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginSend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send).<br/>          |
| [**\_Shell de complemento WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Define la devolución de llamada de Shell para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de Shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell).<br/>       |
| [**\_cierre del complemento WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Define la devolución de llamada de cierre para el complemento.<br/> Todos los complementos de WinRM deben implementar esta función de devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown).<br/>                      |
| [**\_señal del complemento WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Define la devolución de llamada de señal para un complemento.<br/> Todos los complementos de WinRM que admiten funcionalidades de Shell deben implementar esta devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginSignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal).<br/>    |
| [**\_Inicio del complemento WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Define la devolución de llamada de inicio para el complemento.<br/> Todos los complementos de WinRM deben implementar esta función de devolución de llamada.<br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).<br/>                         |



 

 

