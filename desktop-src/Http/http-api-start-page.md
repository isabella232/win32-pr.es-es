---
title: API HTTP Server
description: La API del servidor HTTP permite que las aplicaciones se comuniquen a través de HTTP sin usar Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API HTTP Server
- API del servidor HTTP, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a73d23ffc8f498f4135e07f2b933eddf2896866336a70e11bd9bbf360cacdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950844"
---
# <a name="http-server-api"></a>API HTTP Server

## <a name="purpose"></a>Propósito

La API del servidor HTTP permite que las aplicaciones se comuniquen a través de HTTP sin usar Microsoft Internet Information Server (IIS). Las aplicaciones pueden registrarse para recibir solicitudes HTTP para direcciones URL concretas, recibir solicitudes HTTP y enviar respuestas HTTP. La API del servidor HTTP incluye compatibilidad con SSL para que las aplicaciones puedan intercambiar datos a través de conexiones HTTP seguras sin IIS. También está diseñado para funcionar con puertos de finalización de E/S.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta API está diseñada para su uso por parte de programadores de C/C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API del servidor HTTP se admite en Windows Server 2003 y en Windows XP con Service Pack 2 (SP2). Tenga en cuenta que Microsoft IIS 5 que se ejecuta en Windows XP con SP2 no puede compartir el puerto 80 con otras aplicaciones HTTP que se ejecutan simultáneamente.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                           | Descripción                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Acerca de la API del servidor HTTP](about-http-server-api.md)<br/>                   | Información general sobre HTTP.<br/>                                                              |
| [Uso de LA API del servidor HTTP](using-http-server-api.md)<br/>                   | Guía de procedimientos para usar HTTP.<br/>                                                             |
| [Referencia de LA API del servidor HTTP](http-server-api-reference.md)<br/>           | Documentación de funciones, estructuras y tipos de enumeración específicos disponibles en HTTP.<br/>    |
| [Aplicación de ejemplo de servidor HTTP](http-server-sample-application.md)<br/> | Una aplicación de ejemplo que muestra cómo usar la API del servidor HTTP para realizar tareas del lado servidor.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Servicios HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

