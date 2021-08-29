---
description: Versión remotable del método IMFMediaTypeHandler::GetCurrentMediaType.
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79815747268c8a285e0159017f8f0161926555d09463a3f445b798623137efd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058270"
---
# <a name="remotegetcurrentmediatype"></a>RemoteGetCurrentMediaType

Versión remotable del [**método IMFMediaTypeHandler::GetCurrentMediaType.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a>Comentarios

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) a través de los límites del proceso, el archivo DLL de proxy/stub de Media Foundation convierte la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.

Esta interfaz está disponible en las siguientes plataformas si Windows los componentes redistribuibles del SDK de Media Format 11:

-   Windows XP con Service Pack 2 (SP2) y versiones posteriores.
-   Windows XP Media Center Edition 2005 con KB900325 (Windows XP Media Center Edition 2005) y KB925766 (paquete acumulativo de actualizaciones de octubre de 2006 para Windows XP Media Center Edition) instalados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




