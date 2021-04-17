---
title: Mensaje de WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: El mensaje de configuración de la secuencia de definición de Cap de WM \_ \_ \_ \_ establece los parámetros de configuración que se usan con la captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- Mensaje de WM_CAP_SET_SEQUENCE_SETUP de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535338"
---
# <a name="wm_cap_set_sequence_setup-message"></a>\_Mensaje de \_ instalación de secuencia de conjunto de Cap de \_ WM \_

El mensaje de configuración de la secuencia de definición de Cap de WM establece los parámetros de configuración que se usan con la captura de streaming. **\_ \_ \_ \_** Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .


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

Puntero a una estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre los parámetros que se usan para controlar la captura de streaming, consulte la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

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

 

 





