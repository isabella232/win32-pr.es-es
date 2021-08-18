---
description: Datos específicos del tipo para una secuencia binaria en un archivo de formato de sistemas avanzados (ASF).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826525"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>Atributo MF \_ MT \_ ARBITRARY \_ HEADER

Datos específicos del tipo para una secuencia binaria en un archivo de formato de sistemas avanzados (ASF).

## <a name="data-type"></a>Tipo de datos

**[**MT \_ ENCABEZADO ARBITRARIO \_ almacenado**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** como **BYTE \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentarios

Los archivos ASF pueden contener secuencias con datos binarios. El atributo MF MT ARBITRARY HEADER del tipo de medio contiene una \_ \_ estructura MT \_ [**\_ ARBITRARY \_ HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) que describe la secuencia.

Además del atributo MF MT ARBITRARY HEADER, el tipo de medio para una secuencia binaria \_ \_ de \_ ASF contiene los atributos siguientes:



| Atributo                                                 | Descripción                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MF MT \_ \_**](mf-mt-major-type-attribute.md) | El valor del atributo es **MFMediaType \_ Binary.** |
| [FORMATO \_ ARBITRARIO DE MF MT \_ \_](mf-mt-arbitrary-format.md)   | Contiene datos de formato adicionales.                       |



 

> [!Note]  
> En el SDK Windows formato multimedia, los flujos binarios se denominan *secuencias arbitrarias* o *flujos de datos arbitrarios.*

 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




