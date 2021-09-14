---
title: WM_CAP_FILE_SET_INFOCHUNK mensaje (Vfw.h)
description: El archivo WM \_ CAP \_ FILE SET \_ INFOCHUNK establece y borra los \_ fragmentos de información.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245625"
---
# <a name="wm_cap_file_set_infochunk-message"></a>Mensaje \_ \_ \_ \_ INFOCHUNK de WM CAP FILE SET

El **archivo WM CAP FILE SET \_ \_ \_ \_ INFOCHUNK** establece y borra los fragmentos de información. Los fragmentos de información se pueden insertar en un archivo AVI durante la captura para insertar cadenas de texto o datos personalizados. Puede enviar este mensaje explícitamente o mediante la macro [**capFileSetInfoChunk.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk)


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Puntero a una [**estructura CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) que define el fragmento de información que se va a crear o eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Se pueden agregar varios fragmentos de información registrados a un archivo AVI. Una vez establecido un fragmento de información, se sigue agregando a los archivos de captura posteriores hasta que se borra la entrada o se borran todas las entradas del fragmento de información. Para borrar una sola entrada, especifique el fragmento de información en el miembro **fccInfoID** y **NULL** en el miembro **lpData** de la [**estructura CAPINFOCHUNK.**](/windows/win32/api/vfw/ns-vfw-capinfochunk) Para borrar todas las entradas, especifique **NULL en** **fccInfoID.**

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

 

 





