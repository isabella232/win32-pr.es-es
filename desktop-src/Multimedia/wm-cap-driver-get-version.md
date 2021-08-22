---
title: WM_CAP_DRIVER_GET_VERSION mensaje (Vfw.h)
description: El mensaje GET VERSION del CONTROLADOR \_ DE WM CAP devuelve la información de versión del controlador de captura conectado a una ventana \_ de \_ \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6bed4513383c5dd889639a78e9f00e409fe347bfd6b64b112ea830571ae55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687095"
---
# <a name="wm_cap_driver_get_version-message"></a>Mensaje GET VERSION del CONTROLADOR WM \_ CAP \_ \_ \_

El **mensaje GET VERSION \_ \_ \_ \_ del** CONTROLADOR DE WM CAP devuelve la información de versión del controlador de captura conectado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capDriverGetVersion.**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion)


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, del búfer definido por la aplicación al que hace referencia **szVer.**

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver la información de versión como una cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se realiza **correctamente o FALSE** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Comentarios

La información de versión es una cadena de texto recuperada del área de recursos del controlador. Las aplicaciones deben asignar aproximadamente 40 bytes para esta cadena. Si la información de versión no está disponible, se devuelve una cadena **NULL.**

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

 

 





