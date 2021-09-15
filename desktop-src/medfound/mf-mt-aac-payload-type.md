---
description: Especifica el tipo de carga de una secuencia de codificación de audio avanzada (AAC).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: MF_MT_AAC_PAYLOAD_TYPE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579901"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>Atributo MF \_ MT \_ AAC \_ PAYLOAD \_ TYPE

Especifica el tipo de carga de una secuencia de codificación de audio avanzada (AAC).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Los siguientes valores son posibles.



| Value                                                                        | Significado                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La secuencia solo contiene elementos \_ de bloque de datos sin \_ procesar.<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | Secuencia de transporte de datos de audio (ADTS). La secuencia contiene una secuencia de adts, \_ tal como se define en MPEG-2.<br/>                       |
| <dl> <dt>2</dt> </dl> | Formato de intercambio de datos de audio (ADIF). La secuencia contiene una secuencia de \_ adif, tal como se define en MPEG-2.<br/>                     |
| <dl> <dt>3</dt> </dl> | La secuencia contiene una secuencia de transporte de audio MPEG-4 con una capa de sincronización (LOAS) y una capa multiplex (LATM).<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

MF \_ MT \_ AAC PAYLOAD TYPE es \_ \_ opcional. Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que la secuencia solo contiene elementos \_ de bloque de datos sin \_ procesar.

Solo se aplica a **MFAudioFormat \_ AAC.**

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




