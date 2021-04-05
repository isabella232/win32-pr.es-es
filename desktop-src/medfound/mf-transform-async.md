---
description: Especifica si una transformación de Media Foundation (MFT) realiza el procesamiento asincrónico.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811012"
---
# <a name="mf_transform_async-attribute"></a>MF \_ transformar \_ atributo Async

Especifica si una transformación de Media Foundation (MFT) realiza el procesamiento asincrónico.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

El atributo es un valor booleano:

-   Si el atributo es distinto de cero, el MFT realiza el procesamiento asincrónico.
-   Si el atributo es 0 o no está establecido, el MFT es sincrónico.

Para obtener este atributo, primero llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos de la MFT. Si el método se ejecuta correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el valor del atributo. Si se produce un error en cualquiera de los dos métodos, la MFT es sincrónica.

En el caso de MFTs asincrónico, este atributo debe establecerse en un valor distinto de cero. En el caso de MFTs sincrónicos, este atributo es opcional, pero debe establecerse en 0 si está presente.

Los MFTs asincrónicos no son compatibles con versiones anteriores de Media Foundation. Para usar una MFT asincrónica, el cliente debe establecer el atributo [**MF \_ Transform \_ Async \_ Unlock**](mf-transform-async-unlock.md) en la MFT. (La canalización de Microsoft Media Foundation realiza este paso automáticamente).

## <a name="examples"></a>Ejemplos

El código siguiente comprueba si un MFT realiza el procesamiento asincrónico.


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
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
</dt> <dt>

[**\_desbloqueo asincrónico de transformación MF \_ \_**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




