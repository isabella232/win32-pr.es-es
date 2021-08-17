---
description: Versión remotable del método IMFTopologyNode::GetInputPrefType.
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: RemoteGetInputPrefType (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc11bbb28f15bad78955b59e556873d0500c92e45c126a9e710961ab83cf7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878321"
---
# <a name="remotegetinputpreftype"></a>RemoteGetInputPrefType

Versión remotable del [**método IMFTopologyNode::GetInputPrefType.**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype)

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a>Comentarios

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) a través de los límites del proceso, el archivo DLL de proxy/stub de Media Foundation traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




