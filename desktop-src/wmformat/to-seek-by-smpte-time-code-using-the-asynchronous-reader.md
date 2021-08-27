---
title: Para buscar por código de tiempo de SMPTE mediante el lector asincrónico
description: Para buscar por código de tiempo de SMPTE mediante el lector asincrónico
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por códigos de tiempo de SMPTE
- ASF (formato de sistemas avanzados), búsqueda por códigos de tiempo de SMPTE
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), códigos de tiempo de SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo de SMPTE
- lectores asincrónicos, buscando por códigos de tiempo de SMPTE
- lectores asincrónicos, códigos de tiempo de SMPTE
- Códigos de tiempo de SMPTE, buscar
- Códigos de tiempo de SMPTE, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01ad42170c2458a4dc23a23cfa8102b406f45b6a624cacac28ce31a905ad299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110125"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>Para buscar por código de tiempo de SMPTE mediante el lector asincrónico

El objeto lector puede buscar un punto en un archivo basado en el código de tiempo de SMPTE asociado a una secuencia de vídeo. Los datos de código de tiempo se encapsulan en estructuras DE DATOS DE EXTENSIÓN [**\_ \_ DE \_ CÓDIGO**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) DE TIEMPO DE WMT que se adjuntan a ejemplos de vídeo como extensiones de unidad de datos.

Los códigos de tiempo SMPTE se definen mediante un intervalo y un código de tiempo dentro de ese intervalo. Un intervalo es una serie continua de códigos de tiempo. Cada código de hora se define por horas, minutos, segundos y fotogramas.

Para buscar datos en un archivo ASF mediante código de hora SMPTE mediante el lector asincrónico, realice los pasos siguientes.

1.  Obtenga un puntero a la [**interfaz IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto reader llamando a **IWMReader::QueryInterface**.
2.  Establezca el código de hora de inicio y la duración llamando a [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Debe especificar el número de secuencia de una secuencia de vídeo indizada por código de tiempo. El lector sincronizará el resto de las salidas con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
3.  Controle los ejemplos como lo haría normalmente en la implementación del **método IWMReaderCallback::OnSample.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> <dt>

[**Compatibilidad con código de tiempo de SMPTE**](smpte-time-code-support.md)
</dt> </dl>

 

 




