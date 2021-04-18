---
title: Mensaje de WM_CAP_PAL_OPEN (VFW. h)
description: El \_ \_ \_ mensaje abierto PAL Cap de WM carga una nueva paleta desde un archivo de paleta y la pasa a un controlador de captura.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- Mensaje de WM_CAP_PAL_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665929"
---
# <a name="wm_cap_pal_open-message"></a>\_ \_ Mensaje abierto PAL Cap de WM \_

El **mensaje \_ \_ \_ abierto PAL Cap de WM** carga una nueva paleta desde un archivo de paleta y la pasa a un controlador de captura. Los archivos de paleta suelen utilizar la extensión de nombre de archivo. Señales. Un controlador de captura usa una paleta cuando lo requiere el formato de imagen digitalizada especificado. Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre de archivo de la paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

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

 

 





