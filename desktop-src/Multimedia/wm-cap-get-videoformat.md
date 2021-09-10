---
title: WM_CAP_GET_VIDEOFORMAT mensaje (Vfw.h)
description: El mensaje GET VIDEOFORMAT de WM CAP recupera una copia del formato de vídeo en uso o el \_ tamaño necesario para el formato de \_ \_ vídeo. Puede enviar este mensaje explícitamente o mediante las macros capGetVideoFormat y capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371462"
---
# <a name="wm_cap_get_videoformat-message"></a>Mensaje \_ GET \_ VIDEOFORMAT de WM CAP \_

El **mensaje \_ GET \_ \_ VIDEOFORMAT** de WM CAP recupera una copia del formato de vídeo en uso o el tamaño necesario para el formato de vídeo. Puede enviar este mensaje explícitamente o mediante las macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) y [**capGetVideoFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize)


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, de la estructura a la que hace referencia **s**.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) También puede especificar **NULL para** recuperar el número de bytes necesarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tamaño, en bytes, del formato de vídeo o cero si la ventana de captura no está conectada a un controlador de captura. Para los formatos de vídeo que requieren una paleta, también se devuelve la paleta actual.

## <a name="remarks"></a>Observaciones

Dado que los formatos de vídeo comprimidos varían en los requisitos de tamaño, las aplicaciones deben recuperar primero el tamaño, asignar memoria y, por último, solicitar los datos de formato de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

