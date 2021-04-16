---
title: Puntos de entrada del complemento de autorización
description: Puntos de entrada del complemento de autorización
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee0db76457860106e51bd6c29cead3d0f8227d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714427"
---
# <a name="authorization-plug-in-entry-points"></a>Puntos de entrada del complemento de autorización

Los complementos de autorización se configuran solo para un proceso de host de Internet Information Services (IIS). Solo se puede configurar un complemento de autorización por directorio virtual.

Todos los complementos de autorización deben admitir los siguientes puntos de entrada:

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

El siguiente punto de entrada es opcional:

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

En la tabla siguiente se proporciona información general de los puntos de entrada del complemento de autorización en la API del complemento de Administración remota de Windows (WinRM).



| Función                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_operación de \_ autorización del complemento WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Se llama para autorizar una operación específica. <br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).<br/>                                                                                                                                                                                                       |
| [**la \_ \_ cuota de \_ consulta de autorización del complemento WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Se llama después de que se haya autorizado una conexión para recuperar información de cuota para el usuario. <br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).<br/>                                                                                                                                                    |
| [**\_contexto de \_ versión de autorización del complemento WSMAN \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Se llama para liberar el contexto que un complemento informa de los métodos [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) o [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) . <br/> El nombre del punto de entrada del archivo DLL de este método debe ser [**WSManPluginAuthzReleaseContext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).<br/> |
| [**\_usuario de \_ autorización del complemento WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Se llama para determinar si el usuario puede realizar una solicitud. <br/> El nombre del punto de entrada de la biblioteca de vínculos dinámicos (DLL) de este método debe ser [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).<br/>                                                                                                                                                            |



 

 

