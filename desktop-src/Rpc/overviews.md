---
title: Temas de introducción
description: Página de navegación llamada a procedimiento remoto (RPC) para secciones de información general.
ms.assetid: 49dc35c3-efd7-45a2-bec0-cd68ac150754
keywords:
- Llamada a procedimiento remoto RPC , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97c7735976428ffc4128b0c6a566ac56228921a3bf1070eda69af1579d90b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927564"
---
# <a name="overviews"></a>Temas de introducción

Esta parte de la guía y referencia del programador de llamada a procedimiento remoto (RPC) consta de una secuencia de temas que le ayudarán a comprender la programación de aplicaciones distribuidas y RPC de la siguiente manera:

-   [El modelo RPC de Microsoft](microsoft-rpc-model.md) proporciona información general sobre el modelo de programación cliente-servidor, los estándares para la programación de aplicaciones distribuidas y una descripción de cómo funciona Microsoft RPC.
-   [Instalar el entorno de programación RPC](installing-the-rpc-programming-environment.md) indica cómo instalar los archivos y las herramientas necesarios para desarrollar aplicaciones distribuidas con RPC de Microsoft.
-   [Compilar aplicaciones RPC](building-rpc-applications.md) describe el compilador MIDL y el entorno necesario para compilar aplicaciones distribuidas con Rpc de Microsoft.
-   [La conexión del cliente y el servidor](connecting-the-client-and-the-server.md) proporciona información general sobre el proceso de inicialización y ejecución de aplicaciones distribuidas.
-   [El tutorial](tutorial.md) proporciona información general sobre el desarrollo de una pequeña aplicación distribuida. En este ejemplo se muestran todos los pasos para desarrollar una aplicación distribuida, las herramientas que se usan y los componentes que compartían los programas ejecutables.
-   [Archivos IDL](the-idl-and-acf-files.md) y ACF describe los archivos IDL y ACF que se usan para especificar la interfaz para la llamada a procedimiento remoto y los modificadores del compilador MIDL que controlan cómo se procesan estos archivos.
-   [Características de lenguaje y datos](data-and-language-features.md) muestra el uso de tipos de datos estándar.
-   [Matrices y punteros](arrays-and-pointers.md) explica cómo pasar punteros de matrices como parámetros.
-   [Canalizaciones](pipes.md) describe cómo usar canalizaciones con nombre como mecanismo de transporte para llamadas a procedimientos remotos.
-   [Enlace y identificadores](binding-and-handles.md) describe el identificador de enlace, la estructura de datos que permite al desarrollador enlazar la aplicación que realiza la llamada al procedimiento remoto.
-   [Administración de](memory-management.md) memoria ofrece ideas sobre cómo administrar la memoria en el cliente y el servidor al realizar llamadas a procedimientos remotos.
-   [Servicios de serialización](serialization-services.md) describe los métodos para codificar o codificar datos.
-   [Seguridad](security.md) describe los métodos para implementar características de seguridad en las aplicaciones distribuidas.
-   [En Instalación y configuración de aplicaciones RPC](installing-and-configuring-rpc-applications.md) se describe cómo instalar las aplicaciones cliente y servidor, se describe cómo configurar el proveedor de servicios de nombres y el servicio de seguridad. Esta sección también contiene información de transporte de red para RPC.
-   [RPC asincrónico](asynchronous-rpc.md) presenta información sobre las extensiones asincrónicas de Microsoft a la definición de RPC. Las llamadas a procedimientos remotos asincrónicos se devuelven inmediatamente sin esperar a la salida. Cuando el procedimiento remoto termina de ejecutarse en el servidor, transfiere los datos devueltos al cliente.
-   [RPC Message Queuing](rpc-message-queuing.md) describe el uso de Message Queuing Service (MSMQ), que permite a los usuarios comunicarse entre redes y sistemas independientemente del estado actual de las aplicaciones y sistemas que se comunican.
-   [Llamadas a procedimiento remoto mediante RPC a través](remote-procedure-calls-using-rpc-over-http.md) de HTTP proporciona a los clientes RPC la capacidad de conectarse de forma segura a través de Internet a programas de servidor RPC y ejecutar llamadas a procedimiento remoto.
-   [El equilibrio de carga de RPC](rpc-load-balancing.md) describe la distribución de grandes volúmenes de RPC a través del tráfico HTTP entre numerosos servidores RPC dentro de una granja de servidores.
-   [Los](examples.md) ejemplos contienen una descripción de los programas RPC de ejemplo incluidos con el Kit para desarrolladores de software de plataforma de Microsoft.

 

 




