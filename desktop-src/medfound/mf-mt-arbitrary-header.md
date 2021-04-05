---
description: Datos específicos del tipo de una secuencia binaria en un archivo de formato de sistema avanzado (ASF).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082345"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_Atributo de \_ encabezado arbitrario MF MT \_

Datos específicos del tipo de una secuencia binaria en un archivo de formato de sistema avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

**[**MT \_ \_Encabezado arbitrario**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** almacenado como **byte \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Observaciones

Los archivos ASF pueden contener secuencias con datos binarios. El \_ \_ \_ atributo de encabezado arbitrario MF MT en el tipo de medio contiene una estructura de [**\_ \_ encabezado arbitrario MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) que describe la secuencia.

Además del \_ \_ atributo de encabezado arbitrario MF MT \_ , el tipo de medio de una secuencia binaria ASF contiene los siguientes atributos:



| Atributo                                                 | Descripción                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | El valor del atributo es **MFMediaType \_ Binary**. |
| [\_ \_ formato arbitrario MF \_ MT](mf-mt-arbitrary-format.md)   | Contiene datos de formato adicionales.                       |



 

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
</dt> </dl>

 

 




