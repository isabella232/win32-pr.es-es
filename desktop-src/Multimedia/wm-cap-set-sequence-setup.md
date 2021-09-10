---
title: WM_CAP_SET_SEQUENCE_SETUP mensaje (Vfw.h)
description: El mensaje \_ WM CAP SET SEQUENCE SETUP establece los parámetros de configuración utilizados con la captura de \_ \_ \_ streaming. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371503"
---
# <a name="wm_cap_set_sequence_setup-message"></a>Mensaje DE CONFIGURACIÓN DE SECUENCIA DE SET \_ \_ \_ \_ DE WM CAP

El **mensaje WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP** establece los parámetros de configuración utilizados con la captura de streaming. Puede enviar este mensaje explícitamente o mediante la [**macro capCaptureSetSetup.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, de la estructura a la que hace referencia **s**.

</dd> <dt>

<span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*
</dt> <dd>

Puntero a una [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre los parámetros usados para controlar la captura de streaming, consulte la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

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

 

 





