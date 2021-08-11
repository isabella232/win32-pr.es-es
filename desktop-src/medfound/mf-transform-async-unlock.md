---
description: Habilita el uso de una transformación de Media Foundation asincrónica (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a0a8f328095c3a5c567171fa6a625a77e5623d126dfb2be9f34fef556984be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244181"
---
# <a name="mf_transform_async_unlock-attribute"></a>Atributo MF \_ TRANSFORM \_ ASYNC \_ UNLOCK

Habilita el uso de una transformación de Media Foundation asincrónica (MFT).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Las MTA asincrónicas no son compatibles con versiones anteriores de Microsoft Media Foundation. Para evitar que las aplicaciones existentes utilicen accidentalmente un MFT asincrónico, este atributo debe establecerse en un valor distinto de cero antes de que se pueda usar un MFT asincrónico. La Media Foundation canalización establece automáticamente el atributo , de modo que la mayoría de las aplicaciones no necesitan usar este atributo. Sin embargo, si una aplicación usa un MFT asincrónico fuera de la canalización Media Foundation, la aplicación debe establecer este atributo.

Los MFT sincrónicos no requieren este atributo.

Para probar si un MFT es asincrónico, obtenga el valor del atributo [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md) en MFT.

## <a name="examples"></a>Ejemplos

El código siguiente desbloquea un MFT asincrónico.


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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicos](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




