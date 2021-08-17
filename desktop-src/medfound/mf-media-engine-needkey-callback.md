---
description: Atributo que se pasa en EL ELEMENTO IMFMediaEngineNeedKeyNotify al motor de medios durante la creación.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bec8dd3b802d9fc378d43648ad1d29dd30b6573881a044cc9f0d3aba2015cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956315"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>Atributo \_ \_ \_ NEEDKEY CALLBACK de MF MEDIA ENGINE \_

Atributo que se pasa en [**EL ELEMENTO IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) al motor de medios durante la creación.

## <a name="data-type"></a>Tipo de datos

**IMFMediaEngineNeedKeyNotify \* *_ almacenado como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**a IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentarios

El valor de este atributo es un puntero a la interfaz [**IMFMediaEngineNeedKeyNotify,**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) implementada por la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




