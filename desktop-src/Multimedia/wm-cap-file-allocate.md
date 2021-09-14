---
title: WM_CAP_FILE_ALLOCATE mensaje (Vfw.h)
description: El mensaje \_ WM CAP FILE ALLOCATE crea \_ \_ (preasigna) un archivo de captura de un tamaño especificado. Puede enviar este mensaje explícitamente o mediante la macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161363"
---
# <a name="wm_cap_file_allocate-message"></a>Mensaje \_ WM CAP FILE \_ \_ ALLOCATE

El **mensaje WM CAP FILE \_ \_ \_ ALLOCATE** crea (preasigna) un archivo de captura de un tamaño especificado. Puede enviar este mensaje explícitamente o mediante la [**macro capFileAlloc.**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc)


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

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Puede mejorar significativamente el rendimiento de la captura de streaming mediante la preasignación de un archivo de captura lo suficientemente grande como para almacenar un clip de vídeo completo y desfragmentando el archivo de captura antes de capturar el clip.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





