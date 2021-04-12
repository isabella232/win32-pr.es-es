---
title: Mensaje de WM_CAP_FILE_ALLOCATE (VFW. h)
description: El \_ archivo de Cap de WM \_ \_ asignar mensaje crea (preasigna) un archivo de captura de un tamaño especificado. Puede enviar este mensaje explícitamente o mediante la macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- Mensaje de WM_CAP_FILE_ALLOCATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489748"
---
# <a name="wm_cap_file_allocate-message"></a>\_Mensaje de \_ asignación de archivo Cap de WM \_

El **archivo de Cap de WM \_ \_ \_ asignar** mensaje crea (preasigna) un archivo de captura de un tamaño especificado. Puede enviar este mensaje explícitamente o mediante la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*
</dt> <dd>

Tamaño, en bytes, para crear el archivo de captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Puede mejorar significativamente el rendimiento de la captura de transmisión por secuencias si asigna previamente un archivo de captura lo suficientemente grande como para almacenar un clip de vídeo completo y desfragmenta el archivo de captura antes de capturar el clip.

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

 

 





