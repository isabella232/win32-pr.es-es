---
description: Cuando el Windows Media Audio enumera los tipos de salida, identifica cada tipo enumerado como Estándar, Professional o Sin pérdida de datos.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configuración de la codificación de audio estándar, Professional o sin pérdida de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa4184af8bc6b83710a3710ac1a278de71de0b7221dc11757bdeba46af8c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743542"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Configuración de la codificación de audio estándar, Professional o sin pérdida de datos

Cuando el Windows Media Audio enumera los tipos de salida, identifica cada tipo enumerado como Estándar, Professional o Sin pérdida de datos. Puede determinar si un tipo de salida es Estándar, Professional o Sin pérdida de datos mediante los pasos siguientes.

1.  Llame [**a IMFTransform::GetOutputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) obtener una interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que represente el tipo de salida.
2.  Llame [**a IMFMediaType::GetRepresentation para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) obtener una estructura AM MEDIA [**\_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene información sobre el tipo de salida.
3.  El **miembro pbFormat** de la estructura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) apunta a una estructura [**DE FORMAFORMATEX**](/previous-versions/dd757713(v=vs.85)) que contiene información adicional sobre el tipo de salida. Inspeccione el **miembro wFormatTag** de la **estructura DEFORMATEX.** Un valor de 0x161 indica Estándar, un valor de 0x162 indica Professional y un valor de 0x163 indica Sin pérdida.

Si establece propiedades en el codificador Windows Media Audio antes de enumerar los tipos de salida, puede limitar el número de tipos de salida enumerados. Por ejemplo, si establece las propiedades de VBR correctamente, puede limitar los tipos de salida enumerados a los que se encuentran en la categoría Sin pérdida.

## <a name="standard-audio-encoding"></a>Codificación de audio estándar

Puede usar los pasos siguientes para configurar la codificación de audio estándar.

1.  Establezca las propiedades que prefiera en el codificador.
2.  Enumerar los posibles tipos de salida.
3.  Inspeccione los tipos enumerados y elija uno que tenga una etiqueta de formato de audio 0x161.
4.  Establezca el tipo de salida en el tipo elegido llamando [**a IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Professional Codificación de audio

Puede usar los pasos siguientes para configurar la codificación Professional audio.

1.  Establezca las propiedades que prefiera en el codificador.
2.  Enumerar los posibles tipos de salida.
3.  Inspeccione los tipos enumerados y elija uno que tenga una etiqueta de formato de audio 0x162.
4.  Establezca el tipo de salida en el tipo elegido llamando [**a IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Codificación de audio sin pérdida

Puede usar los pasos siguientes para configurar la codificación de audio sin pérdida.

1.  Establezca la [**propiedad MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **VARIANT \_ TRUE.**
2.  Establezca la [**propiedad MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) en **VARIANT \_ TRUE.**
3.  Establezca la [**propiedad \_ MFPKEY DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) en 100.
4.  Enumerar los tipos de salida.
5.  Establezca el tipo de salida en uno de los tipos enumerados en el paso 4 llamando a [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

El código siguiente enumera todos los tipos de salida sin pérdida para el codificador Windows Media Audio. El código imprime el valor de la etiqueta de formato de audio para cada tipo enumerado. Dado que todos los tipos enumerados no tienen pérdidas, todas esas etiquetas de formato tienen un valor de 0x163. Suponga que pIMT es un puntero a una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un objeto de codificador Windows Media Audio y que pStore es un puntero a una **interfaz IPropertyStore** en el mismo objeto. Supongamos también que hr es una variable de tipo **HRESULT** que se declaró anteriormente en el código.


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

 

 
