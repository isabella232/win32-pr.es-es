---
description: Especifica el tipo de carga de una secuencia de codificación de audio avanzada (AAC).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: MF_MT_AAC_PAYLOAD_TYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721579"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>\_Atributo de \_ \_ tipo de carga de módulo MF MT AAC \_

Especifica el tipo de carga de una secuencia de codificación de audio avanzada (AAC).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Los valores siguientes son posibles.



| Value                                                                        | Significado                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | El flujo solo contiene \_ elementos de bloque de datos sin procesar \_ .<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | Secuencia de transporte de datos de audio (ADTS). La secuencia contiene una \_ secuencia ADTS, tal y como se define en MPEG-2.<br/>                       |
| <dl> <dt>2</dt> </dl> | Formato de intercambio de datos de audio (ADIF). La secuencia contiene una \_ secuencia Adif, tal y como se define en MPEG-2.<br/>                     |
| <dl> <dt>3</dt> </dl> | La secuencia contiene una secuencia de transporte de audio MPEG-4 con una capa de sincronización (Loa) y una capa de multiplexación (LATM).<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

El \_ \_ tipo de carga AAC MT AAC \_ \_ es opcional. Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que la secuencia contiene \_ solo elementos de bloque de datos sin procesar \_ .

Solo se aplica a **MFAudioFormat \_ AAC**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




