---
description: Versión remotable del método IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS.
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581052"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a>RemoteEndUnregisterTopologyWorkQueuesWithMMCSS

Versión remotable del método [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS.**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss)

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Observaciones

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) a través de los límites del proceso, el archivo DLL de proxy/stub de Media Foundation convierte la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




