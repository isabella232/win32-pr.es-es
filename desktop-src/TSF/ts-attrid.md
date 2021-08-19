---
title: TS_ATTRID (Textstor.h)
description: El tipo de datos ATTRID de TS \_ se usa para identificar un atributo de texto.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1c40d56f1f8ff3deb59d0dd7664a197a672ade7b2d53beebd8e35ba5de7c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950341"
---
# <a name="ts_attrid"></a>TS \_ ATTRID

El **tipo de datos \_ ATTRID de TS** se usa para identificar un atributo de texto.


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>Comentarios

Hay una lista de GUID predefinidos para \_ TS ATTRID en tsattrs.h.

Los GUID TSATTRID Text VerticalWriting y \_ \_ TSATTRID Text Orientation son útiles para que las aplicaciones coincidan con el texto de entrada que se \_ va a \_ corregir. Se pueden crear GUID adicionales definidos por el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                             |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITextStoreACP::FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP::RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP::RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP::RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink::OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[**ITextStoreAnchor::FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[**ITextStoreAnchorSink::OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[**ATTRVAL de TS \_**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





