---
description: Contiene los nombres descriptivos de los estilos de intercambio multimedia accesible sincronizado (SAMI) definidos en el archivo SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f57d418eb86c19d3aa2db12808dde810456c38ec6abd45fbece450b30f60f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876178"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>Atributo MF \_ PD \_ SAMI \_ STYLELIST

Contiene los nombres descriptivos de los estilos de intercambio multimedia accesible sincronizado (SAMI) definidos en el archivo SAMI.

El [origen de medios SAMI](sami-media-source.md) establece este atributo en el descriptor de presentación que crea.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

El blob de atributos tiene la siguiente estructura:



Tipo de datos

Descripción

Tamaño (bytes)

**DWORD**

Número de cadenas de estilo.

4

Para cada cadena de estilo:

**DWORD**

Tamaño de la cadena en bytes, incluido el **carácter NULL.**

4

**LPWSTR**

Cadena de caracteres anchos terminada en NULL que contiene el nombre del estilo.

Varía



 

Para establecer el estilo o recuperar el estilo actual, use la [**interfaz IMFSAMIStyle.**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="examples"></a>Ejemplos


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Origen multimedia SAMI](sami-media-source.md)
</dt> </dl>

 

 




