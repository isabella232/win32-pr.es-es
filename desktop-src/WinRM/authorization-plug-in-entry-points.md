---
title: Puntos de entrada del complemento de autorización
description: Puntos de entrada del complemento de autorización
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16ca861df6b6546920aaf3f778c61117776ff3861556377b280c990c03711fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324083"
---
# <a name="authorization-plug-in-entry-points"></a>Puntos de entrada del complemento de autorización

Los complementos de autorización solo se configuran para un proceso Internet Information Services host de Internet Information Services (IIS). Solo se puede configurar un complemento de autorización por directorio virtual.

Todos los complementos de autorización deben admitir los siguientes puntos de entrada:

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

El siguiente punto de entrada es opcional:

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

En la tabla siguiente se proporciona información general sobre los puntos de entrada del complemento de autorización en Windows Remote Management (WinRM) Plug-in API.



| Función                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPERACIÓN DE AUTORIZACIÓN DEL COMPLEMENTO WSMAN \_ \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Se llama para autorizar una operación específica. <br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).<br/>                                                                                                                                                                                                       |
| [**CUOTA DE CONSULTAS DE AUTORIZACIÓN DEL COMPLEMENTO WSMAN \_ \_ \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Se llama después de que se haya autorizado una conexión para recuperar información de cuota para el usuario. <br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).<br/>                                                                                                                                                    |
| [**CONTEXTO DE VERSIÓN DE AUTORIZACIÓN DEL COMPLEMENTO WSMAN \_ \_ \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Se llama para liberar el contexto que un complemento notifica de los métodos [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) o [**WSManPluginAuthzOperationComplete.**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) <br/> El nombre del punto de entrada dll para este método debe ser [**WSManPluginAuthzReleaseContext.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context)<br/> |
| [**AUTORIZACIÓN DEL \_ USUARIO EN EL COMPLEMENTO WSMAN \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Se llama para determinar si el usuario puede llevar a cabo una solicitud. <br/> El nombre del punto de entrada de la biblioteca de vínculos dinámicos (DLL) para este método debe ser [**WSManPluginAuthzUser.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)<br/>                                                                                                                                                            |



 

 

