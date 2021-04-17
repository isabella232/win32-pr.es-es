---
title: Para pausar o detener la reproducción
description: Para pausar o detener la reproducción
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF), pausar la reproducción
- ASF (formato de sistemas avanzados), pausar la reproducción
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), detener la reproducción
- ASF (formato de sistemas avanzados), detener la reproducción
- Advanced Systems Format (ASF), reproducción en pausa o detención
- ASF (formato de sistemas avanzados), reproducción en pausa o detención
- lectores asincrónicos, pausar la reproducción
- lectores asincrónicos, detener la reproducción
- lectores asincrónicos, reproducción en pausa o detención
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532980"
---
# <a name="to-pause-or-stop-playback"></a>Para pausar o detener la reproducción

Al llamar a [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) para empezar a reproducir un archivo, el lector asincrónico continuará el procesamiento en sus propios subprocesos independientes hasta que se alcance el final del archivo. Puede pausar o detener la entrega de muestras mediante los métodos [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) o [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) , respectivamente.

## <a name="pausing"></a>Pausando

Cuando se llama a **IWMReader::P ause** para pausar la reproducción de un archivo, el lector realiza un seguimiento de la posición actual en el archivo. Para reanudar la reproducción después de la pausa, llame a [**IWMReader:: resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). La reproducción se reanudará desde el punto en el que se ha pausado.

## <a name="stopping"></a>Deteniéndose

Cuando se llama a **IWMReader:: Stop** para detener la reproducción de un archivo, el lector no realiza un seguimiento de la información sobre el progreso de la reproducción. Para usar **detener** y volver al punto de detención, debe guardar el tiempo de presentación del último ejemplo entregado y usarlo en la llamada a **IWMReader:: Start**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




