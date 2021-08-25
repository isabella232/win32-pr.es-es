---
description: Especifica si una transformación Media Foundation (MFT) realiza el procesamiento asincrónico.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a647ca122c138f2ef7e90670798200fc3fa629be48d6242b4e71dbc93151e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714355"
---
# <a name="mf_transform_async-attribute"></a>Atributo MF \_ TRANSFORM \_ ASYNC

Especifica si una transformación Media Foundation (MFT) realiza el procesamiento asincrónico.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

El atributo es un valor booleano:

-   Si el atributo es distinto de cero, MFT realiza el procesamiento asincrónico.
-   Si el atributo es 0 o no está establecido, el MFT es sincrónico.

Para obtener este atributo, primero llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos de MFT. Si ese método se realiza correctamente, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el valor del atributo. Si se produce un error en cualquiera de los dos métodos, MFT es sincrónico.

Para las MTA asincrónicas, este atributo debe establecerse en un valor distinto de cero. En el caso de las MTA sincrónicas, este atributo es opcional, pero debe establecerse en 0 si está presente.

Las MTO asincrónicas no son compatibles con versiones anteriores de Media Foundation. Para usar un MFT asincrónico, el cliente debe establecer el atributo [**MF \_ TRANSFORM \_ ASYNC \_ UNLOCK**](mf-transform-async-unlock.md) en MFT. (La Microsoft Media Foundation realiza este paso automáticamente).

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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> <dt>

[**DESBLOQUEO \_ ASINCRÓNICO DE TRANSFORMACIÓN DE \_ \_ MF**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




