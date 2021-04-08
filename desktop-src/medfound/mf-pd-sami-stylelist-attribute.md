---
description: Contiene los nombres descriptivos de los estilos de intercambio de medios accesibles (SAMI) sincronizados definidos en el archivo SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913165"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>MF \_ PD \_ Sami \_ STYLELIST (atributo)

Contiene los nombres descriptivos de los estilos de intercambio de medios accesibles (SAMI) sincronizados definidos en el archivo SAMI.

El [origen de medios Sami](sami-media-source.md) establece este atributo en el descriptor de presentación que crea.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El BLOB de atributo tiene la estructura siguiente:



Tipo de datos

Descripción

Tamaño (bytes)

**DWORD**

Número de cadenas de estilo.

4

Para cada cadena de estilo:

**DWORD**

Tamaño de la cadena en bytes, incluido el carácter **nulo** .

4

**LPWSTR**

Cadena de caracteres anchos terminada en null que contiene el nombre del estilo.

Varía



 

Para establecer el estilo o recuperar el estilo actual, use la interfaz [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Origen de medios SAMI](sami-media-source.md)
</dt> </dl>

 

 




