---
description: Versión remotable del método IMFSourceResolver::BeginCreateObjectFromURL.
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: RemoteBeginCreateObjectFromURL (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d8f7fe0827041e38e37cb27fee5b334a3763b63ca2c2568e393e6ad5796b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013925"
---
# <a name="remotebegincreateobjectfromurl"></a>RemoteBeginCreateObjectFromURL

Versión remotable del [**método IMFSourceResolver::BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Comentarios

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) a través de los límites del proceso, el archivo DLL de proxy/stub de Media Foundation traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




