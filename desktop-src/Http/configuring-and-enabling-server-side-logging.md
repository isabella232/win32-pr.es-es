---
title: Configuración y habilitación del registro del lado servidor
description: Configuración y habilitación del registro del lado servidor
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418678"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configuración y habilitación del registro del lado servidor

La aplicación habilita el registro en la sesión de servidor o el grupo de direcciones URL antes de enviar la respuesta con [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). En el ejemplo siguiente se muestra cómo configurar y habilitar el registro del lado servidor de tipo W3C:

1.  La aplicación inicializa la estructura [**de \_ \_ información de registro http**](/windows/desktop/api/Http/ns-http-http_logging_info) con **HttpLoggingTypeW3C** especificado en el miembro de **formato** y una máscara de máscara de las constantes de [**\_ \_ campo de registro http**](http-log-field--constants.md) en el miembro **Fields** .
2.  La aplicación llama a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerLoggingProperty** especificado en el parámetro *Property* y un puntero a la estructura de [**\_ \_ información de registro http**](/windows/desktop/api/Http/ns-http-http_logging_info) en el parámetro *pPropertyInformation* .

La máscara de la las constantes de [**\_ \_ campo de registro http**](http-log-field--constants.md) contiene los campos que se pueden registrar en el archivo de registro de W3C. Tenga en cuenta que el establecimiento de la propiedad **HttpServerLoggingProperty** en una sesión de servidor o un grupo de direcciones URL no significa que se registrarán las respuestas http. El registro se realiza en función de cada solicitud cuando W3C está habilitado en la llamada a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

Para habilitar el registro de respuestas de W3C en función de cada solicitud, la aplicación realiza los pasos siguientes:

1.  La aplicación inicializa los miembros de los datos de los [**\_ \_ campos \_ de registro http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) con la información de campo que se registrará para esa respuesta.
2.  El miembro **base. Type** de la estructura de [**datos de \_ \_ campos \_ de registro http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) se debe inicializar en **HttpLogDataTypeFields**. El campo **base. Type** garantiza la extensibilidad futura de la estructura y la API.
3.  La aplicación llama a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) con un puntero a la estructura de datos de [**campos de \_ Registro \_ \_ http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) en el parámetro *pLogData* . La aplicación debe escribir el puntero en los [**\_ \_ datos de registro de PHTTP**](/windows/desktop/api/Http/ns-http-http_log_data).

 

 




