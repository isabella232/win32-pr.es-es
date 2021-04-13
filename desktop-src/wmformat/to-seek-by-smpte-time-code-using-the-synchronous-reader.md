---
title: Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico
description: Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF), búsqueda por códigos de tiempo de SMPTE
- ASF (formato de sistemas avanzados), búsqueda por códigos de tiempo de SMPTE
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- lectores sincrónicos, búsquedas por códigos de tiempo de SMPTE
- lectores sincrónicos, códigos de tiempo SMPTE
- Códigos de tiempo de SMPTE, búsqueda
- Códigos de tiempo de SMPTE, lectores sincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358704"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico

El objeto de lector sincrónico puede buscar en un punto de un archivo basándose en el código de tiempo SMPTE asociado con una secuencia de vídeo. Los datos de código de tiempo se encapsulan en las estructuras de [**\_ datos de extensión de código de tiempo \_ \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que se adjuntan a los ejemplos de vídeo como extensiones de unidad de datos.

Los códigos de tiempo de SMPTE se definen mediante un intervalo y un código de tiempo dentro de ese intervalo. Un intervalo es una serie continua de códigos de tiempo. Cada código de tiempo se define por horas, minutos, segundos y fotogramas.

Para buscar datos en un archivo ASF por código de tiempo SMPTE mediante el lector sincrónico, realice los pasos siguientes.

1.  Establezca el código de tiempo de inicio y el código de hora de finalización para la entrega de ejemplo llamando a [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Debe especificar el número de secuencia de un flujo de vídeo indexado por código de tiempo. El lector sincrónico sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada.
2.  Comience a recuperar ejemplos con llamadas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Continúe como lo haría normalmente con el lector sincrónico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Compatibilidad con código de tiempo SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




