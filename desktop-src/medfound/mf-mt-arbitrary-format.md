---
description: Datos de formato adicionales para una secuencia binaria en un archivo de formato de sistemas avanzados (ASF).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7629e92eea07059f562d553985628f2099df1da03bd371617f0eed5183dd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973614"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>Atributo \_ MF MT \_ ARBITRARY \_ FORMAT

Datos de formato adicionales para una secuencia binaria en un archivo de formato de sistemas avanzados (ASF).

## <a name="data-type"></a>Tipo de datos

**Byte\[\]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentarios

Las aplicaciones pueden usar flujos binarios para contener tipos de datos personalizados. El origen multimedia de ASF trata el valor de este atributo como un blob opaco. El **miembro formattype** de la [**estructura MT \_ ARBITRARY \_ HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) define el diseño de los datos de formato.

Esta estructura corresponde al campo Datos de formato de los datos específicos del tipo en el objeto Propiedades de secuencia, en archivos donde el tipo de secuencia es Medios **\_ binarios \_ de ASF.** Para más información, consulte la especificación de ASF.

> [!Note]  
> En el SDK Windows formato multimedia, los flujos binarios se denominan *secuencias arbitrarias* o *flujos de datos arbitrarios.*

 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[ENCABEZADO \_ ARBITRARIO MF MT \_ \_](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




