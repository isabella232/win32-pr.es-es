---
title: Mensaje de WM_CAP_PAL_SAVE (VFW. h)
description: El mensaje de guardado de PAL de Cap de WM \_ \_ \_ guarda la paleta actual en un archivo de paleta. Los archivos de paleta suelen utilizar la extensión de nombre de archivo. Señales. Puede enviar este mensaje explícitamente o mediante la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- Mensaje de WM_CAP_PAL_SAVE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666028"
---
# <a name="wm_cap_pal_save-message"></a>\_Mensaje de \_ guardado de PAL de Cap de WM \_

El mensaje de guardado de PAL de Cap de WM guarda la paleta actual en un archivo de paleta. **\_ \_ \_** Los archivos de paleta suelen utilizar la extensión de nombre de archivo. Señales. Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .


```C++
WM_CAP_PAL_SAVE 
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

 

 





