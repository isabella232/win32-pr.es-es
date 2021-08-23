---
description: Introducción a la arquitectura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Introducción a la arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eafce326655a4d9386d37c02df9ef0ab2b9772b5e87eedaff40a19383b2cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590475"
---
# <a name="architecture-overview"></a>Introducción a la arquitectura

La arquitectura de WPD se puede dividir en tres procesos. Dentro de estos procesos se encuentran los tres componentes principales de WPD: la API, el serializador y el controlador. En la ilustración siguiente se muestran los procesos y componentes que constituyen la arquitectura de WPD.

![ilustración que muestra los componentes api, serializer y driver de wpd](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>Interfaz de programación de aplicaciones WPD

La API de WPD se implementa como un servidor COM en proceso. La API usa las API estándar de Microsoft Win32 para comunicarse con el controlador WPD adecuado. Tanto los objetos de API como el controlador usan un componente denominado serializador WPD para empaquetar o desempaquetar parámetros hacia o desde búferes de Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF).

## <a name="the-wpd-serializer"></a>Serializador de WPD

El serializador WPD se implementa como un servidor COM en proceso. La API de WPD usa el serializador para empaquetar comandos y parámetros en búferes de mensajes que se envían al controlador. El controlador usa el serializador para desempaquetar estos búferes de mensajes para su procesamiento. El controlador también usa el serializador para empaquetar datos y parámetros en búferes de respuesta que se devuelven a la API de WPD, y la API de WPD usa el serializador para desempaquetar estos búferes de respuesta para volver a los llamadores.

## <a name="wpd-driver"></a>Controlador WPD

El controlador WPD se implementa como un controlador estándar Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF). LOS controladores WPD se hospedan mediante UMDF en un proceso independiente denominado Host de controlador.

El controlador recibe mensajes del reflector UMDF (esto no se muestra en el diagrama, ya que la forma en que se reciben los búferes no es importante para el controlador. Consulte la documentación de UMDF para obtener más información). El controlador implementa un controlador de código de control de E/S (IOCL) específico de WPD para procesar los mensajes DE WPD recibidos por la API de WPD. El controlador usa el serializador WPD para desempaquetar comandos y parámetros de estos búferes de mensajes y empaquetar la respuesta en el búfer de retorno.

Los controladores de WPD pueden comunicarse con sus dispositivos pasando por un controlador en modo kernel, al que normalmente se accede a través de operaciones de archivo Win32 (es decir, CreateFile, ReadFile, WriteFile, y así sucesivamente). En el caso de los buses comunes, Microsoft proporcionará controladores de kernel estándar para que los proveedores los usen, lo que permitirá a los proveedores enviar una solución de controlador solo en modo de usuario. Además, para los dispositivos MTP (Media Transfer Protocol) y Mass Storage Class (MSC), Microsoft proporcionará controladores de clase WPD.

Para obtener más información sobre los controladores de WPD, vea la documentación Windows Portable Devices Driver en Windows Driver Kit.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción a la aplicación**](application-overview.md)
</dt> </dl>

 

 



