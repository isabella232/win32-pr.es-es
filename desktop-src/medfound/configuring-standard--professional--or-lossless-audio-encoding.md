---
description: Cuando el codificador de Windows Media Audio enumera los tipos de salida, identifica cada tipo enumerado como estándar, profesional o sin pérdida.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configuración de la codificación de audio estándar, profesional o sin pérdida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808150"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Configuración de la codificación de audio estándar, profesional o sin pérdida

Cuando el codificador de Windows Media Audio enumera los tipos de salida, identifica cada tipo enumerado como estándar, profesional o sin pérdida. Puede determinar si un tipo de salida es Standard, Professional o Lossless realizando los pasos siguientes.

1.  Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener una interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que represente el tipo de salida.
2.  Llame a [**IMFMediaType:: GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) para obtener una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contenga información sobre el tipo de salida.
3.  El miembro **pbFormat** de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) apunta a una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que contiene información adicional sobre el tipo de salida. Inspeccione el miembro **wFormatTag** de la estructura **WAVEFORMATEX** . Un valor de 0x161 indica Standard, un valor de 0x162 indica Professional y un valor de 0x163 indica Lossless.

Si establece propiedades en el codificador Windows Media Audio antes de enumerar los tipos de salida, puede limitar el número de tipos de salida que se enumeran. Por ejemplo, si establece las propiedades de VBR adecuadamente, puede limitar los tipos de salida enumerados a los que se encuentran en la categoría sin pérdida.

## <a name="standard-audio-encoding"></a>Codificación de audio estándar

Puede usar los pasos siguientes para configurar la codificación de audio estándar.

1.  Establezca las propiedades de su elección en el codificador.
2.  Enumera los posibles tipos de salida.
3.  Inspeccione los tipos enumerados y elija uno que tenga una etiqueta de formato de audio de 0x161.
4.  Establezca el tipo de salida en el tipo elegido llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Codificación de audio profesional

Puede usar los pasos siguientes para configurar la codificación de audio profesional.

1.  Establezca las propiedades de su elección en el codificador.
2.  Enumera los posibles tipos de salida.
3.  Inspeccione los tipos enumerados y elija uno que tenga una etiqueta de formato de audio de 0x162.
4.  Establezca el tipo de salida en el tipo elegido llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Codificación de audio sin pérdida

Puede usar los pasos siguientes para configurar la codificación de audio sin pérdida.

1.  Establezca la propiedad [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **Variant \_ true**.
2.  Establezca la propiedad [**MFPKEY de \_ restricción \_ enumerada \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) en **Variant \_ true**.
3.  Establezca la [**propiedad \_ \_ VBRQUALITY deseada de MFPKEY**](mfpkey-desired-vbrqualityproperty.md) en 100.
4.  Enumerar los tipos de salida.
5.  Establezca el tipo de salida en uno de los tipos enumerados en el paso 4 llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

En el código siguiente se enumeran todos los tipos de salida sin pérdida para el codificador Windows Media Audio. El código imprime el valor de la etiqueta de formato de audio para cada tipo enumerado. Dado que todos los tipos enumerados son sin pérdida, todas esas etiquetas de formato tienen un valor de 0x163. Supongamos que pIMT es un puntero a una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un objeto de codificador Windows Media Audio y que pStore es un puntero a una interfaz **IPropertyStore** en el mismo objeto. Supongamos también que HR es una variable de tipo **HRESULT** que se declaró anteriormente en el código.


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de audio](configuringaudioencoding.md)
</dt> </dl>

 

 
