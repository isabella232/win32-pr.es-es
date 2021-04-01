---
title: Constantes de TS_IE_ (Textstor. h)
description: Las constantes de TS \_ IE \_ \ describen cómo insertar texto que puede contener objetos incrustados utilizados por servicios de texto.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150094"
---
# <a name="ts_ie_-constants"></a>\_Constantes de IE de TS \_ \*

Las constantes de IE de TS \_ \_ \* describen cómo insertar texto que puede contener objetos incrustados utilizados por servicios de texto.



| Constante o valor                                                                                                                                                                                                                          | Descripción                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <dt>**TS \_ \_Corrección de IE**</dt> <dt>(0x1)</dt> </dl>    | El texto es una transformación (corrección) de contenido existente y se conserva cualquier información de marcado de texto (metadatos) especial, como datos de archivos. WAV o un identificador de idioma.<br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <dt>**TS \_ \_Composición de IE**</dt> <dt>(0X2)</dt> </dl> | No se utiliza.<br/>                                                                                                                                                                  |



## <a name="remarks"></a>Observaciones

Estas constantes se utilizan en el parámetro *dwFlags* de [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) y [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





