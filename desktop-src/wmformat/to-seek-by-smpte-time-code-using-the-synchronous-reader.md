---
title: Para buscar por código de tiempo SMPTE mediante el lector sincrónico
description: Para buscar por código de tiempo SMPTE mediante el lector sincrónico
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), búsqueda por códigos de tiempo SMPTE
- Formato de sistemas avanzados (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Formato de sistemas avanzados (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- lectores sincrónicos, en busca de códigos de tiempo SMPTE
- lectores sincrónicos, códigos de tiempo SMPTE
- Códigos de tiempo SMPTE, buscar
- Códigos de tiempo SMPTE, lectores sincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b368492d45d3bc564ce0fbb84a6013349c26fcdaca8c1ad576863a9cee6f6f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196474"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Para buscar por código de tiempo SMPTE mediante el lector sincrónico

El objeto de lector sincrónico puede buscar un punto en un archivo basado en el código de tiempo SMPTE asociado a una secuencia de vídeo. Los datos de código de tiempo se encapsulan en estructuras DE DATOS DE EXTENSIÓN DE CÓDIGO DE TIEMPO [**\_ \_ DE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que se adjuntan a ejemplos de vídeo como extensiones de unidad de datos.

Los códigos de tiempo SMPTE se definen mediante un intervalo y un código de tiempo dentro de ese intervalo. Un intervalo es una serie continua de códigos de tiempo. Cada código de hora se define por horas, minutos, segundos y fotogramas.

Para buscar datos en un archivo ASF mediante código de tiempo SMPTE mediante el lector sincrónico, realice los pasos siguientes.

1.  Establezca el código de hora de inicio y el código de hora de finalización para la entrega de ejemplo mediante una llamada [**a IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Debe especificar el número de secuencia de una secuencia de vídeo indizada por código de tiempo. El lector sincrónico sincronizará el resto de las salidas con el tiempo de presentación del marco especificado de la secuencia especificada.
2.  Comience a recuperar ejemplos con llamadas a [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Continúe como lo haría normalmente con el lector sincrónico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Compatibilidad con código de tiempo de SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




