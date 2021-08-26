---
description: Versión remotable del método IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS.
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93a5d969dda1323d8ddb5f313fabbf482651ccd4bb966a922e0c4f0f734ebde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013915"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a>RemoteEndUnregisterPlatformWorkQueueWithMMCSS

Versión remotable del método [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS.**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss)

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Comentarios

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) a través de los límites del proceso, el archivo DLL de proxy/stub de Media Foundation convierte la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




