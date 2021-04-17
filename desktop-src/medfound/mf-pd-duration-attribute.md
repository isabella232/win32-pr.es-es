---
description: Especifica la duración de una presentación, en unidades de 100-nanosegundos.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: MF_PD_DURATION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716418"
---
# <a name="mf_pd_duration-attribute"></a>\_Atributo de \_ duración MF PD

Especifica la duración de una presentación, en unidades de 100-nanosegundos.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="remarks"></a>Observaciones

Los orígenes multimedia pueden establecer este atributo en un descriptor de presentación para indicar la duración de la presentación.

Este atributo es un valor con signo, aunque se almacena como **UINT64**. Sin embargo, el atributo nunca debe contener un valor negativo.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo obtener la duración de la presentación desde un origen de multimedia.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




