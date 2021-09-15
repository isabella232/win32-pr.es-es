---
title: WM_CAP_DRIVER_GET_NAME mensaje (Vfw.h)
description: El mensaje WM \_ CAP DRIVER GET NAME devuelve el nombre del controlador de captura conectado a la ventana de \_ \_ \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473851"
---
# <a name="wm_cap_driver_get_name-message"></a>Mensaje GET \_ \_ NAME DEL CONTROLADOR \_ WM CAP \_

El **mensaje WM CAP DRIVER GET \_ \_ \_ \_ NAME** devuelve el nombre del controlador de captura conectado a la ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capDriverGetName.**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname)


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver el nombre del dispositivo como una cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Observaciones

El nombre es una cadena de texto recuperada del área de recursos del controlador. Las aplicaciones deben asignar aproximadamente 80 bytes para esta cadena. Si el controlador no contiene un recurso de nombre, se devuelve el nombre completo de la ruta de acceso del controlador que aparece en el registro o en SYSTEM.INI archivo.

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

 

 





