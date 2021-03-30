---
title: Por qué usar DirectShow
description: Por qué usar DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, hardware
- SDK de Windows Media Format, Modelo de controlador de Windows (WDM)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), hardware
- ASF (formato de sistemas avanzados), hardware
- Advanced Systems Format (ASF), Modelo de controlador de Windows (WDM)
- ASF (formato de sistemas avanzados), Modelo de controlador de Windows (WDM)
- DirectShow, acerca de
- DirectShow, hardware
- DirectShow, Modelo de controlador de Windows (WDM)
- Modelo de controlador de Windows (WDM)
- WDM (Modelo de controlador de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775907"
---
# <a name="why-use-directshow"></a>¿Por qué usar DirectShow?

Hay dos razones principales por las que una aplicación puede usar DirectShow en lugar del SDK de Windows Media Format directamente: para la comodidad de la arquitectura de streaming de DirectShow y para el acceso al hardware.

## <a name="convenience"></a>Comodidad

Con la arquitectura de streaming de DirectShow, solo realiza algunas llamadas a métodos para reproducir Windows Media Audio o Windows Media Video archivos. También se simplifica la creación de archivos. Solo tiene que especificar un perfil mediante la interfaz **IConfigAsfWriter** en el filtro y DirectShow carga automáticamente los componentes necesarios para representar o escribir las secuencias, y proporciona los mecanismos para transferir y sincronizar el flujo de datos multimedia. DirectShow es especialmente útil al convertir contenido de formatos variados al formato de Windows Media. Puede crear gráficos de filtros de DirectShow que descodifiquen una amplia variedad de tipos de archivos y de compresión y, a continuación, alimentar los flujos descodificados en el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) . Por comparación, el ejemplo UncompAVItoWMV de este SDK solo funciona con archivos AVI sin comprimir. Los flujos de texto y los flujos de datos arbitrarios también se pueden crear o representar mediante DirectShow, pero esto podría requerir la creación de filtros de DirectShow personalizados para procesar esas secuencias.

## <a name="access-to-hardware"></a>Acceso al hardware

DirectShow es la única manera de que el código de aplicación acceda a los dispositivos de hardware basados en Modelo de controlador de Windows (WDM), como cámaras DV de 1394, sintonizadores de TV y webcams USB. Si la aplicación debe capturar datos directamente desde un dispositivo de hardware basado en WDM y transcodificarlos en el formato de Windows Media, y el SDK de Windows Media Encoder no se adapta a sus necesidades, DirectShow es la única alternativa. DirectShow también puede usarse para tener acceso a dispositivos heredados basados en vídeo para Windows.

 

 




