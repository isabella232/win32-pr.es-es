---
description: Especifica si una Media Foundation transformación de datos (MFT) realiza el procesamiento asincrónico.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360450"
---
# <a name="mf_transform_async-attribute"></a>Atributo MF \_ TRANSFORM \_ ASYNC

Especifica si una Media Foundation transformación de datos (MFT) realiza el procesamiento asincrónico.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

El atributo es un valor booleano:

-   Si el atributo es distinto de cero, MFT realiza el procesamiento asincrónico.
-   Si el atributo es 0 o no está establecido, el MFT es sincrónico.

Para obtener este atributo, primero llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos de MFT. Si ese método se realiza correctamente, llame [**a IMFAttributes::GetUINT32 para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) obtener el valor del atributo. Si se produce un error en cualquiera de los dos métodos, MFT es sincrónico.

Para las MTA asincrónicas, este atributo debe establecerse en un valor distinto de cero. En el caso de las MTA sincrónicas, este atributo es opcional, pero debe establecerse en 0 si está presente.

Las MTA asincrónicas no son compatibles con versiones anteriores de Media Foundation. Para usar un MFT asincrónico, el cliente debe establecer el atributo [**MF \_ TRANSFORM \_ ASYNC \_ UNLOCK**](mf-transform-async-unlock.md) en MFT. (La Microsoft Media Foundation de datos realiza este paso automáticamente).

## <a name="examples"></a>Ejemplos

El código siguiente comprueba si un MFT realiza un procesamiento asincrónico.


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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicos](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> <dt>

[**DESBLOQUEO \_ ASINCRÓNICO DE TRANSFORMACIÓN DE \_ \_ MF**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




