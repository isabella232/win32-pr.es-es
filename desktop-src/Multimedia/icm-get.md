---
title: ICM_GET mensaje (Vfw.h)
description: El ICM GET recupera un valor DWORD definido por la aplicación \_ de un controlador de compresión de vídeo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8885faf7b0605378ace3004165004384a582c9d49a0a8ce047122c108b6cb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038735"
---
# <a name="icm_get-message"></a>\_ICM Mensaje GET

El **ICM \_ get** recupera un valor **DWORD** definido por la aplicación de un controlador de compresión de vídeo.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Puntero a un bloque de memoria que se va a rellenar con el estado actual. También puede especificar **NULL para** determinar la cantidad de memoria necesaria para la información de estado.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Tamaño, en bytes, del bloque de memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de memoria, en bytes, necesaria para almacenar la información de estado.

## <a name="remarks"></a>Comentarios

La estructura utilizada para representar la información de estado es específica del controlador y la define el controlador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





