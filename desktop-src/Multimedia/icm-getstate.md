---
title: ICM_GETSTATE mensaje (Vfw.h)
description: El ICM GETSTATE consulta un controlador de compresión de vídeo para devolver su configuración actual en un bloque de memoria o para determinar la cantidad de memoria necesaria para recuperar la información \_ de configuración.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246254"
---
# <a name="icm_getstate-message"></a>\_ICM Mensaje GETSTATE

El **ICM \_ getstate** consulta un controlador de compresión de vídeo para devolver su configuración actual en un bloque de memoria o para determinar la cantidad de memoria necesaria para recuperar la información de configuración. Puede enviar este mensaje explícitamente o mediante la macro [**ICGetState.**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Puntero a un bloque de memoria para contener la información de configuración actual. Puede especificar **NULL para** este parámetro para determinar la cantidad de memoria necesaria para la información de configuración, como en [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Tamaño, en bytes, del bloque de memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si *pv* es **NULL,** devuelve la cantidad de memoria, en bytes, necesaria para la información de configuración.

Si *pv* no es **NULL,** devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

La estructura utilizada para representar la información de configuración es específica del controlador y la define el controlador.

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

 

 





