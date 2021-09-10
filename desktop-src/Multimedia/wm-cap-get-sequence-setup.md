---
title: WM_CAP_GET_SEQUENCE_SETUP mensaje (Vfw.h)
description: El mensaje GET SEQUENCE SETUP de WM \_ CAP recupera la configuración actual de los parámetros de captura de \_ \_ \_ streaming. Puede enviar este mensaje explícitamente o mediante la macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371449"
---
# <a name="wm_cap_get_sequence_setup-message"></a>Mensaje \_ DE CONFIGURACIÓN GET SEQUENCE \_ \_ \_ DE WM CAP

El **mensaje GET SEQUENCE SETUP \_ \_ \_ \_ de WM CAP** recupera la configuración actual de los parámetros de captura de streaming. Puede enviar este mensaje explícitamente o mediante la [**macro capCaptureGetSetup.**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup)


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, de la estructura a la que hace referencia **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*s*
</dt> <dd>

Puntero a una [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre los parámetros usados para controlar la captura de streaming, vea la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

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

 

 





