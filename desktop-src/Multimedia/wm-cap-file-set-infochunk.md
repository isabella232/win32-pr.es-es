---
title: Mensaje de WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: El archivo Cap de WM establece el \_ \_ \_ conjunto \_ de mensajes INFOCHUNK y borra fragmentos de información.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- Mensaje de WM_CAP_FILE_SET_INFOCHUNK de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078898"
---
# <a name="wm_cap_file_set_infochunk-message"></a>\_ \_ \_ Mensaje INFOCHUNK de conjunto de archivos Cap de WM \_

El **archivo Cap de WM establece el conjunto de mensajes \_ \_ \_ \_ INFOCHUNK** y borra fragmentos de información. Se pueden insertar fragmentos de información en un archivo AVI durante la captura para insertar cadenas de texto o datos personalizados. Puede enviar este mensaje explícitamente o mediante la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Puntero a una estructura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) que define el fragmento de información que se va a crear o eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Se pueden agregar varios fragmentos de información registrados a un archivo AVI. Después de establecer un fragmento de información, sigue siendo agregado a los archivos de captura posteriores hasta que se borre la entrada o se borren todas las entradas de fragmentos de información. Para borrar una sola entrada, especifique el fragmento de información en el miembro **fccInfoID** y **null** en el miembro **lpData** de la estructura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) . Para borrar todas las entradas, especifique **null** en **fccInfoID**.

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

 

 





