---
description: Habilita el uso de una transformación de Media Foundation asincrónica (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363887"
---
# <a name="mf_transform_async_unlock-attribute"></a>Atributo MF \_ TRANSFORM \_ ASYNC \_ UNLOCK

Habilita el uso de una transformación de Media Foundation asincrónica (MFT).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Las MTO asincrónicas no son compatibles con versiones anteriores de Microsoft Media Foundation. Para evitar que las aplicaciones existentes utilicen accidentalmente un MFT asincrónico, este atributo debe establecerse en un valor distinto de cero antes de poder usar un MFT asincrónico. La Media Foundation de datos establece automáticamente el atributo, de modo que la mayoría de las aplicaciones no necesitan usar este atributo. Sin embargo, si una aplicación usa un MFT asincrónico fuera de la canalización Media Foundation, la aplicación debe establecer este atributo.

Las MTA sincrónicas no requieren este atributo.

Para probar si un MFT es asincrónico, obtenga el valor del atributo [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md) en el MFT.

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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




