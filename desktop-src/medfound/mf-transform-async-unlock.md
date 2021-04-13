---
description: Habilita el uso de una transformación de Media Foundation asincrónica (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543227"
---
# <a name="mf_transform_async_unlock-attribute"></a>MF \_ transformar \_ \_ atributo Async Unlock

Habilita el uso de una transformación de Media Foundation asincrónica (MFT).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Los MFTs asincrónicos no son compatibles con versiones anteriores de Microsoft Media Foundation. Para evitar que las aplicaciones existentes usen accidentalmente un MFT asincrónico, este atributo debe establecerse en un valor distinto de cero antes de que se pueda usar una MFT asincrónica. La canalización de Media Foundation establece automáticamente el atributo, de modo que la mayoría de las aplicaciones no necesitan usar este atributo. Sin embargo, si una aplicación usa un MFT asincrónico fuera de la canalización de Media Foundation, la aplicación debe establecer este atributo.

Los MFTs sincrónicos no requieren este atributo.

Para probar si una MFT es asincrónica, obtenga el valor del atributo [MF \_ Transform \_ Async](mf-transform-async.md) en la MFT.

## <a name="examples"></a>Ejemplos

El código siguiente desbloquea una MFT asincrónica.


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrónico](asynchronous-mfts.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




