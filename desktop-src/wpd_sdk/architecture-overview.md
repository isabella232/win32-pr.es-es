---
description: Introducción a la arquitectura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Introducción a la arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912889"
---
# <a name="architecture-overview"></a>Introducción a la arquitectura

La arquitectura de WPD puede dividirse en tres procesos. Dentro de estos procesos se encuentran los tres componentes principales de WPD: la API, el serializador y el controlador. En la ilustración siguiente se muestran los procesos y los componentes que constituyen la arquitectura de WPD.

![Ilustración en la que se muestran los componentes de API, serializador y controlador de WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>La interfaz de programación de aplicaciones de WPD

La API de WPD se implementa como un servidor COM en proceso. La API usa las API estándar de Microsoft Win32 para comunicarse con el controlador de WPD adecuado. Un componente denominado serializador de WPD lo usan los objetos de la API y el controlador para empaquetar o desempaquetar los parámetros de los búferes del marco de trabajo de controladores de modo de usuario (UMDF) de Windows Driver Foundation (WDF).

## <a name="the-wpd-serializer"></a>El serializador de WPD

El serializador de WPD se implementa como un servidor COM en proceso. La API de WPD usa el serializador para empaquetar comandos y parámetros en los búferes de mensajes que se envían al controlador. El controlador usa el serializador para desempaquetar estos búferes de mensajes para su procesamiento. El controlador también usa el serializador para empaquetar datos y parámetros en búferes de respuesta que se devuelven a la API de WPD, y la API de WPD usa el serializador para desempaquetar estos búferes de respuesta y volver a los llamadores.

## <a name="wpd-driver"></a>Controlador de WPD

El controlador WPD se implementa como un controlador estándar de controlador de modo de usuario (UMDF) de Windows Driver Foundation (WDF). Los controladores de WPD se hospedan en UMDF en un proceso independiente denominado host de controlador.

El controlador recibe mensajes desde el reflector UMDF (esto no se muestra en el diagrama, ya que el modo en que se reciben los búferes no es importante para el controlador). Consulte la documentación de UMDF para obtener más información). El controlador implementa un controlador de código de control de e/s (IOCL) específico de WPD para procesar los mensajes de WPD recibidos por la API de WPD. El controlador usa el serializador de WPD para desempaquetar los comandos y parámetros de estos búferes de mensajes y para empaquetar la respuesta en el búfer de retorno.

Los controladores de WPD pueden comunicarse con sus dispositivos pasando por un controlador de modo kernel, al que normalmente se tiene acceso a través de operaciones de archivo Win32 (es decir, CreateFile, ReadFile, WriteFile, etc.). En el caso de los buses comunes, Microsoft proporcionará controladores de kernel estándar para que los usen los proveedores, lo que permitirá a los proveedores enviar una solución de controladores solo en modo de usuario. Además, en el caso de los dispositivos de protocolo de transferencia de medios (MTP) y de clase de almacenamiento masivo (MSC), Microsoft proporcionará controladores de clase de WPD.

Para obtener más información acerca de los controladores de WPD, consulte la documentación del controlador de dispositivos portátiles de Windows en el kit de controladores de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general de la aplicación**](application-overview.md)
</dt> </dl>

 

 



