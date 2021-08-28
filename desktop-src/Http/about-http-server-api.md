---
title: Acerca de LA API del servidor HTTP
description: La API de servidor HTTP proporciona a los desarrolladores una interfaz de bajo nivel en el lado servidor de la funcionalidad HTTP, tal como se define en RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API de servidor HTTP, información general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55883fa75b366a2f5c5ef434f1eef3a95651440738735b025cfe5ef1b0534106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015013"
---
# <a name="about-http-server-api"></a>Acerca de LA API del servidor HTTP

La API de servidor HTTP proporciona a los desarrolladores una interfaz de bajo nivel en el lado servidor de la funcionalidad HTTP, tal como se define en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). La API permite a una aplicación recibir solicitudes HTTP dirigidas a direcciones URL y enviar respuestas HTTP. Para enviar respuestas dinámicas, se recomiendan las interfaces ISAPI o ASP.NET interfaz.

La API del servidor HTTP permite que varias aplicaciones coexistan en un sistema, compartiendo el mismo puerto TCP (por ejemplo, el puerto 80 para HTTP o el puerto 443 para HTTPS) y atendiendo diferentes partes del espacio de nombres de dirección URL.

La API del servidor HTTP requiere conocimiento del lenguaje de programación C y una familiaridad con la programación Windows API. Las aplicaciones que no requieren acceso de bajo nivel a HTTP deben usar la ISAPI de IIS o las .NET Framework para las soluciones basadas en HTTP.

 

 




