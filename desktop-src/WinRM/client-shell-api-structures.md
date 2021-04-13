---
title: Definiciones y estructuras de API de Shell de cliente
description: En la tabla siguiente se proporciona información general sobre las estructuras y otras definiciones de la API del shell de cliente de Administración remota de Windows (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00a908856a6df8233e377d917ff28029dc8468e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420869"
---
# <a name="client-shell-api-structures-and-definitions"></a>Definiciones y estructuras de API de Shell de cliente

En la tabla siguiente se proporciona información general sobre las estructuras y otras definiciones de la API del shell de cliente de Administración remota de Windows (WinRM).



| Función                                                                      | Descripción                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_función de \_ finalización del shell WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Función de devolución de llamada a la que se llama para las operaciones de Shell, lo que da como resultado una solicitud remota. |



 



| Estructura                                                                      | Descripción                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_credenciales de autenticación de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Define el método de autenticación y las credenciales usadas para la autenticación de servidor o proxy.                                              |
| [**datos de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Almacena los datos entrantes y salientes usados en la API de WinRM.                                                                                     |
| [**\_binario de datos WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Almacena datos binarios para su uso con varias funciones de la API de WinRM.                                                                                |
| [**\_texto de datos de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Almacena datos basados en texto para su uso con varias funciones de la API de WinRM.                                                                            |
| [**\_variable de entorno de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Define una variable de entorno individual mediante un par de nombre y valor.                                                                  |
| [**\_conjunto de \_ variables de entorno de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Define una matriz de variables de entorno.                                                                                                  |
| [**ERROR de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contiene información de error.                                                                                                                 |
| [**\_clave WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Representa un par de clave y valor dentro de un conjunto de selector y se utiliza para identificar un recurso determinado.                                       |
| [**WSMAN ( \_ opción)**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Representa un par de nombre y valor de opción específico.                                                                                           |
| [**\_conjunto de opciones de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Representa un conjunto de opciones.                                                                                                                |
| [**\_información del proxy WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Establece la información de proxy para cada sesión.                                                                                                |
| [**\_resultado de recepción de \_ datos de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Representa los datos de salida recibidos de la API de [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) .                                |
| [**\_datos de respuesta de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Representa los datos de salida recibidos de una operación de [**WSMan**](wsman.md) .                                                                |
| [**\_conjunto de selector de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Define un conjunto de claves que representan la identidad de un recurso.                                                                            |
| [**Shell de WSMAN \_ \_ Async**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Define una estructura asincrónica que se pasa a todas las operaciones de Shell.                                                                   |
| [**\_información de \_ desconexión del shell WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**\_información de \_ Inicio del shell de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Almacena todos los datos específicos del shell necesarios para crear un shell mediante la llamada del complemento [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) . |
| [**\_conjunto de \_ identificadores de secuencia WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Muestra todas las secuencias que se usan para la entrada o salida del shell y los comandos.                                                  |
| [**\_ \_ credenciales de contraseña de nombre de usuario WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Define las credenciales usadas para la autenticación.                                                                                            |



 

 

 