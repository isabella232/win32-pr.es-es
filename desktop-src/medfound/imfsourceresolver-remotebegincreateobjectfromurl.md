---
description: 'Versión remota del método IMFSourceResolver:: BeginCreateObjectFromURL.'
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: RemoteBeginCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d9a72ab5522b56fc0b78238f6a1dbc9aae0c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705839"
---
# <a name="remotebegincreateobjectfromurl"></a>RemoteBeginCreateObjectFromURL

Versión remota del método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Observaciones

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla vtable de la interfaz. Si se llama a [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




