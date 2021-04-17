---
description: Datos de formato adicionales para una secuencia binaria en un archivo de formato de sistema avanzado (ASF).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716355"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>Atributo de formato de MF \_ MT \_ arbitrario \_

Datos de formato adicionales para una secuencia binaria en un archivo de formato de sistema avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

**BYTES\[\]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden usar secuencias binarias para contener tipos de datos personalizados. El origen de medios ASF trata el valor de este atributo como un BLOB opaco. El miembro **formatType** de la estructura de [**\_ \_ encabezado arbitraria de MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) define el diseño de los datos de formato.

Esta estructura corresponde al campo de datos de formato de los datos específicos del tipo en el objeto de propiedades de la secuencia, en archivos donde el tipo de secuencia es un **\_ \_ medio binario ASF**. Para obtener más información, consulte la especificación ASF.

> [!Note]  
> En el SDK de Windows Media Format, las secuencias binarias se denominan *flujos arbitrarios* o *flujos de datos arbitrarios*.

 

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[\_ \_ encabezado arbitrario MF \_ MT](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




