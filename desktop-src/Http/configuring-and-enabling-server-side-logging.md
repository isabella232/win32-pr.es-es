---
title: Configuración y habilitación del registro del lado servidor
description: Configuración y habilitación del registro del lado servidor
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95856cf72379de44211f05bb78fb4c6839f77b2fd6c42b91b26068bc9c5d0d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050815"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configuración y habilitación del registro del lado servidor

La aplicación habilita el registro en la sesión del servidor o el grupo de direcciones URL antes de enviar la respuesta [**con HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). En el ejemplo siguiente se muestra cómo configurar y habilitar el registro del lado servidor de tipo W3C:

1.  La aplicación inicializa la estructura [**HTTP \_ LOGGING \_ INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) con **HttpLoggingTypeW3C** especificado en el miembro **Format** y una máscara de bits de las constantes [**HTTP LOG \_ \_ FIELD**](http-log-field--constants.md) en el **miembro Fields.**
2.  La aplicación llama a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerLoggingProperty** especificado en el parámetro *Property* y un puntero a la estructura [**HTTP \_ LOGGING \_ INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) en el *parámetro pPropertyInformation.*

La máscara de bits de las [**constantes \_ HTTP LOG \_ FIELD**](http-log-field--constants.md) contiene los campos que se pueden registrar en el archivo de registro W3C. Tenga en cuenta que establecer **la propiedad HttpServerLoggingProperty** en una sesión de servidor o un grupo de direcciones URL no significa que se registrarán las respuestas HTTP. El registro se realiza por solicitud cuando W3C está habilitado en la llamada a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Para habilitar el registro de respuestas de W3C por solicitud, la aplicación realiza los pasos siguientes:

1.  La aplicación inicializa los miembros de [**HTTP \_ LOG FIELDS \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) con la información de campo que se registrará para esa respuesta.
2.  El **miembro Base.Type** de la estructura [**HTTP LOG FIELDS \_ \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) debe inicializarse en **HttpLogDataTypeFields.** El **campo Base.Type** garantiza la extensibilidad futura de la estructura y la API.
3.  La aplicación llama a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) con un puntero a la estructura [**HTTP LOG FIELDS \_ \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) en el *parámetro pLogData.* La aplicación debe convertir el puntero a [**PHTTP \_ LOG \_ DATA.**](/windows/desktop/api/Http/ns-http-http_log_data)

 

 




