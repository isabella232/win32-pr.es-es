---
title: Mensaje de WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: El \_ mensaje Cap de WM \_ obtener \_ videoformat recupera una copia del formato de vídeo en uso o el tamaño necesario para el formato de vídeo. Puede enviar este mensaje explícitamente o mediante las macros capGetVideoFormat y capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- Mensaje de WM_CAP_GET_VIDEOFORMAT de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996359"
---
# <a name="wm_cap_get_videoformat-message"></a>\_Mensaje de \_ obtención de formato de Cap \_ de WM

El **mensaje \_ Cap de WM \_ obtener \_ videoformat** recupera una copia del formato de vídeo en uso o el tamaño necesario para el formato de vídeo. Puede enviar este mensaje explícitamente o mediante las macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) y [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .


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

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . También puede especificar **null** para recuperar el número de bytes necesarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tamaño, en bytes, del formato de vídeo o cero si la ventana de captura no está conectada a un controlador de captura. En el caso de los formatos de vídeo que requieran una paleta, también se devuelve la paleta actual.

## <a name="remarks"></a>Observaciones

Dado que los formatos de vídeo comprimidos varían en cuanto a los requisitos de tamaño, las aplicaciones deben recuperar primero el tamaño, asignar la memoria y, por último, solicitar los datos de formato de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

