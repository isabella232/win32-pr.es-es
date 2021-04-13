---
title: Para recuperar ejemplos de medios con el lector sincrónico
description: Para recuperar ejemplos de medios con el lector sincrónico
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF), recuperar ejemplos de medios
- ASF (formato de sistemas avanzados), recuperar ejemplos de medios
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, recuperar ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420268"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Para recuperar ejemplos de medios con el lector sincrónico

Debe solicitar cada ejemplo de uno en uno desde el lector sincrónico. Esto le proporciona más control sobre los ejemplos que recibe y cuándo los recibe.

Use el método [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) para recuperar un ejemplo. Debe pasar principalmente punteros a variables que se rellenarán con información sobre el ejemplo recuperado como parámetros. El único parámetro de entrada es *wStreamNum*. Si pasa un número de secuencia, **GetNextSample** recuperará el siguiente ejemplo con el número de secuencia especificado. Si pasa cero para *wStreamNum*, se recupera el siguiente ejemplo que se produce cronológicamente en el archivo.

De forma predeterminada, el lector sincrónico recupera todos los ejemplos de las salidas de un archivo en orden cronológico. Si llama a **GetNextSample** y no hay más ejemplos para obtener, devolverá NS \_ E \_ ningún \_ ejemplo más \_ , que es un código de error erróneo. Al codificar por lo tanto, simplemente puede recorrer los ejemplos hasta que se produzca un error en el método.

> [!Note]  
> Para asegurarse de que el lector sincrónico ofrezca duraciones de ejemplo correctas para las secuencias de vídeo, primero debe configurar la salida de la secuencia. Llame al método [**IWMSyncReader:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) para establecer el valor de g \_ wszVideoSampleDurations en **true**.

 

Código de ejemplo

En el ejemplo de código siguiente se muestra cómo usar **GetNextSample** para recuperar todos los ejemplos de un archivo.


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

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




