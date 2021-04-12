---
title: Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico
description: Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF), búsqueda por códigos de tiempo de SMPTE
- ASF (formato de sistemas avanzados), búsqueda por códigos de tiempo de SMPTE
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- lectores asincrónicos, búsquedas por códigos de tiempo de SMPTE
- lectores asincrónicos, códigos de tiempo SMPTE
- Códigos de tiempo de SMPTE, búsqueda
- Códigos de tiempo de SMPTE, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420233"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico

El objeto lector puede buscar en un punto de un archivo basándose en el código de tiempo SMPTE asociado con una secuencia de vídeo. Los datos de código de tiempo se encapsulan en las estructuras de [**\_ datos de extensión de código de tiempo \_ \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que se adjuntan a los ejemplos de vídeo como extensiones de unidad de datos.

Los códigos de tiempo de SMPTE se definen mediante un intervalo y un código de tiempo dentro de ese intervalo. Un intervalo es una serie continua de códigos de tiempo. Cada código de tiempo se define por horas, minutos, segundos y fotogramas.

Para buscar datos en un archivo ASF mediante código de tiempo SMPTE mediante el lector asincrónico, realice los pasos siguientes.

1.  Obtenga un puntero a la interfaz [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto lector llamando a **IWMReader:: QueryInterface**.
2.  Establezca el código de tiempo de inicio y la duración mediante una llamada a [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Debe especificar el número de secuencia de un flujo de vídeo que se indexa por código de tiempo. El lector sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
3.  Controle los ejemplos como lo haría normalmente en su implementación del método **IWMReaderCallback::** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> <dt>

[**Compatibilidad con código de tiempo SMPTE**](smpte-time-code-support.md)
</dt> </dl>

 

 




