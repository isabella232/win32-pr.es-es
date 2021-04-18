---
title: Temas de introducción
description: Página de navegación de llamada a procedimiento remoto (RPC) para las secciones de información general.
ms.assetid: 49dc35c3-efd7-45a2-bec0-cd68ac150754
keywords:
- RPC llamada a procedimiento remoto, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea90c08dc075fdd90ae604b0d347ba6ac5baf9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357444"
---
# <a name="overviews"></a>Temas de introducción

Esta parte de la guía y referencia del programador de llamada a procedimiento remoto (RPC) consta de una secuencia de temas que le ayudarán a comprender la programación de aplicaciones distribuidas y RPC de la siguiente manera:

-   El [modelo RPC de Microsoft](microsoft-rpc-model.md) proporciona información general sobre el modelo de programación cliente-servidor, estándares para la programación de aplicaciones distribuidas y una descripción de cómo funciona Microsoft RPC.
-   [La instalación del entorno de programación RPC](installing-the-rpc-programming-environment.md) indica cómo instalar los archivos y herramientas necesarios para desarrollar aplicaciones distribuidas con Microsoft RPC.
-   La [compilación de aplicaciones RPC](building-rpc-applications.md) describe el compilador MIDL y el entorno necesario para compilar aplicaciones distribuidas con Microsoft RPC.
-   Al [conectar el cliente y el servidor,](connecting-the-client-and-the-server.md) se proporciona información general del proceso de inicialización y ejecución de aplicaciones distribuidas.
-   En este [tutorial](tutorial.md) se proporciona información general sobre el desarrollo de una pequeña aplicación distribuida. En este ejemplo se muestran todos los pasos para desarrollar una aplicación distribuida, las herramientas que se usan y los componentes que componen los programas ejecutables.
-   [Archivos IDL y ACF](the-idl-and-acf-files.md) describe los archivos IDL y ACF que se usan para especificar la interfaz para la llamada a procedimiento remoto y los modificadores de compilador MIDL que controlan cómo se procesan estos archivos.
-   Los [datos y las características del lenguaje](data-and-language-features.md) muestran el uso de tipos de datos estándar.
-   [Matrices y punteros](arrays-and-pointers.md) explica cómo pasar punteros de matrices como parámetros.
-   [Canalizaciones](pipes.md) describe cómo usar canalizaciones con nombre como mecanismo de transporte para las llamadas a procedimientos remotos.
-   [Enlace y identificadores](binding-and-handles.md) describe el identificador de enlace: la estructura de datos que permite al desarrollador enlazar la aplicación que realiza la llamada al procedimiento remoto.
-   La [Administración de memoria](memory-management.md) ofrece ideas sobre cómo administrar la memoria en el cliente y el servidor al realizar llamadas a procedimientos remotos.
-   [Servicios de serialización](serialization-services.md) describe los métodos para codificar o descodificar datos.
-   [Seguridad](security.md) describe los métodos para implementar características de seguridad en las aplicaciones distribuidas.
-   [Instalación y configuración de aplicaciones RPC](installing-and-configuring-rpc-applications.md) describe la instalación de las aplicaciones de cliente y servidor, que describe cómo configurar el proveedor de servicios de nombres y el servicio de seguridad. Esta sección también contiene información de transporte de red para RPC.
-   [RPC asincrónico](asynchronous-rpc.md) presenta información acerca de las extensiones asincrónicas de Microsoft para la definición de RPC. Las llamadas asincrónicas a procedimientos remotos devuelven inmediatamente sin esperar a la salida. Cuando el procedimiento remoto termina de ejecutarse en el servidor, transfiere los datos devueltos al cliente.
-   [Message Queue Server de RPC](rpc-message-queuing.md) describe el uso del servicio de Message Queue Server (MSMQ), que permite a los usuarios comunicarse a través de redes y sistemas, independientemente del estado actual de las aplicaciones y los sistemas que se comunican.
-   Las [llamadas a procedimientos remotos mediante RPC a través de http](remote-procedure-calls-using-rpc-over-http.md) proporcionan a los clientes RPC la capacidad de conectarse de forma segura a través de Internet a programas de servidor RPC y ejecutar llamadas a procedimientos remotos.
-   El [equilibrio de carga de RPC](rpc-load-balancing.md) describe la distribución de grandes volúmenes de tráfico de RPC a través de http entre numerosos servidores RPC en una granja de servidores.
-   Los [ejemplos](examples.md) contienen una descripción de los programas RPC de ejemplo que se incluyen con el kit del desarrollador de software de la plataforma de Microsoft.

 

 




