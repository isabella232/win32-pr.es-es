---
title: Para recuperar ejemplos de medios con el lector sincrónico
description: Para recuperar ejemplos de medios con el lector sincrónico
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Formato de sistemas avanzados (ASF), recuperación de ejemplos multimedia
- ASF (formato de sistemas avanzados), recuperación de ejemplos multimedia
- Formato de sistemas avanzados (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, recuperación de ejemplos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1ec4fc7e8a894de304ea828cef9d8e019f4cdedfd2fbd851a427382ba741a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807435"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Para recuperar ejemplos de medios con el lector sincrónico

Debe solicitar cada muestra de una en una desde el lector sincrónico. Esto le proporciona más control sobre los ejemplos que recibe y cuándo los recibe.

Use el [**método IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) para recuperar un ejemplo. Debe pasar principalmente punteros a variables que se rellenarán con información sobre el ejemplo recuperado como parámetros. El único parámetro de entrada *es wStreamNum.* Si pasa un número de secuencia, **GetNextSample** recuperará el ejemplo siguiente con el número de secuencia especificado. Si pasa cero para *wStreamNum*, se recupera el ejemplo siguiente que se produce cronológicamente en el archivo.

De forma predeterminada, el lector sincrónico recupera todos los ejemplos de las salidas en un archivo en orden cronológico. Si llama a **GetNextSample** y no hay más ejemplos para obtener, devolverá NS E NO MORE SAMPLES, que es un código \_ de error con \_ \_ \_ errores. Por lo tanto, al codificar, simplemente puede recorrer los ejemplos hasta que se produce un error en el método.

> [!Note]  
> Para asegurarse de que el lector sincrónico proporciona duraciones de ejemplo correctas para las secuencias de vídeo, primero debe configurar la salida de la secuencia. Llame al [**método IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) para establecer el valor g \_ wszVideoSampleDurations en **TRUE.**

 

Código de ejemplo

En el código de ejemplo siguiente se muestra cómo usar **GetNextSample** para recuperar todos los ejemplos de un archivo.


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




