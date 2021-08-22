---
title: Estructuras y definiciones de la API de Shell de cliente
description: En la tabla siguiente se proporciona información general sobre las estructuras y otras definiciones de la API de shell de cliente Windows administración remota (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643265"
---
# <a name="client-shell-api-structures-and-definitions"></a>Estructuras y definiciones de la API de Shell de cliente

En la tabla siguiente se proporciona información general sobre las estructuras y otras definiciones de la API de shell de cliente Windows administración remota (WinRM).



| Función                                                                      | Descripción                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**FUNCIÓN DE FINALIZACIÓN \_ DEL SHELL \_ DE WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Función de devolución de llamada a la que se llama para las operaciones de shell, lo que resulta en una solicitud remota. |



 



| Estructura                                                                      | Descripción                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**CREDENCIALES DE \_ AUTENTICACIÓN DE WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Define el método de autenticación y las credenciales usadas para la autenticación de servidor o proxy.                                              |
| [**WSMAN \_ DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Almacena los datos entrantes y salientes que se usan en la API de WinRM.                                                                                     |
| [**WSMAN \_ DATA \_ BINARY**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Almacena datos binarios para su uso con varias funciones de la API de WinRM.                                                                                |
| [**TEXTO DE DATOS DE WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Almacena datos basados en texto para su uso con varias funciones de la API de WinRM.                                                                            |
| [**VARIABLE DE ENTORNO DE WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Define una variable de entorno individual mediante un par de nombre y valor.                                                                  |
| [**CONJUNTO DE \_ VARIABLES DE ENTORNO \_ DE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Define una matriz de variables de entorno.                                                                                                  |
| [**ERROR DE WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contiene información de error.                                                                                                                 |
| [**WSMAN \_ KEY**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Representa un par clave-valor dentro de un conjunto de selectores y se usa para identificar un recurso determinado.                                       |
| [**WSMAN \_ OPTION**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Representa un par de nombre y valor de opción específico.                                                                                           |
| [**WSMAN \_ OPTION \_ SET**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Representa un conjunto de opciones.                                                                                                                |
| [**WSMAN \_ PROXY \_ INFO**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Establece la información del proxy para cada sesión.                                                                                                |
| [**WSMAN \_ RECEIVE \_ DATA \_ RESULT**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Representa los datos de salida recibidos de la API [**WSManReceiveShellOutput.**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)                                |
| [**DATOS DE RESPUESTA DE WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Representa los datos de salida recibidos de una [**operación de WSMan.**](wsman.md)                                                                |
| [**CONJUNTO DE \_ SELECTORES DE WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Define un conjunto de claves que representan la identidad de un recurso.                                                                            |
| [**WSMAN \_ SHELL \_ ASYNC**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Define una estructura asincrónica que se pasa a todas las operaciones de shell.                                                                   |
| [**INFORMACIÓN DE \_ DESCONEXIÓN DE WSMAN SHELL \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | Por determinar                                                                                                                                         |
| [**INFORMACIÓN DE INICIO \_ DE WSMAN SHELL \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Almacena todos los datos específicos del shell necesarios para crear un shell mediante la llamada del complemento [**WSManCreateShell.**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) |
| [**CONJUNTO DE \_ IDENTIFICADORES DE \_ FLUJO DE WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Enumera todos los flujos que se usan para la entrada o salida del shell y los comandos.                                                  |
| [**\_CREDS DE CONTRASEÑA DE NOMBRE DE USUARIO DE \_ \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Define las credenciales usadas para la autenticación.                                                                                            |



 

 

 