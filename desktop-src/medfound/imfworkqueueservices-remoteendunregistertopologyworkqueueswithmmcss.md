---
description: Versión remotable del método IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS.
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f083b4c0d7ae5610b041c14b3e6e54b917fdf7570300a5d7973a096b803bc447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941905"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a>RemoteEndUnregisterTopologyWorkQueuesWithMMCSS

Versión remotable del método [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS.**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss)

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Comentarios

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) a través de los límites del proceso, el archivo DLL de proxy/stub de Media Foundation convierte la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




