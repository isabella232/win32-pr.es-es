---
title: Para pausar o detener la reproducción
description: Para pausar o detener la reproducción
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Formato de sistemas avanzados (ASF), pausar la reproducción
- ASF (formato de sistemas avanzados), pausar la reproducción
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), detener la reproducción
- ASF (formato de sistemas avanzados), detener la reproducción
- Formato de sistemas avanzados (ASF), pausa o detención de la reproducción
- ASF (formato de sistemas avanzados), pausar o detener la reproducción
- lectores asincrónicos, pausar la reproducción
- lectores asincrónicos, detener la reproducción
- lectores asincrónicos, pausa de reproducción o detención
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7ae7f3c1dd2c045a35b8d3ee8950ace849a032136371f9da7ff1bcc2b12de27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845370"
---
# <a name="to-pause-or-stop-playback"></a>Para pausar o detener la reproducción

Cuando se llama a [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) para empezar a reproducir un archivo, el lector asincrónico continuará procesando en sus propios subprocesos independientes hasta que se alcance el final del archivo. Puede pausar o detener la entrega de ejemplos mediante los métodos [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) o [**IWMReader::Stop,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) respectivamente.

## <a name="pausing"></a>Pausando

Cuando se llama a **IWMReader::P ause** para pausar la reproducción de un archivo, el lector realiza un seguimiento de la posición actual en el archivo. Para reanudar la reproducción después de pausar, llame [**a IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). La reproducción se reanudará desde el punto en el que se detuvo.

## <a name="stopping"></a>Deteniéndose

Cuando se llama a **IWMReader::Stop** para detener la reproducción de un archivo, el lector no realiza un seguimiento de ninguna información sobre el progreso de la reproducción. Para usar **Detener** y volver posteriormente al punto de detención, debe guardar el tiempo de presentación del último ejemplo entregado y usarlo en la llamada a **IWMReader::Start**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lectura de archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




