---
title: ICM_SETSTATE mensaje (Vfw.h)
description: El ICM SETSTATE notifica a un controlador de compresión \_ de vídeo que establezca el estado del resalte. Puede enviar este mensaje explícitamente o mediante la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea6cd7aa0314520a30e293a8f029920c22b8baa58e995eed7ff9e5a96dd1b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525815"
---
# <a name="icm_setstate-message"></a>\_ICM Mensaje SETSTATE

El **ICM \_ SETSTATE** notifica a un controlador de compresión de vídeo que establezca el estado del resalte. Puede enviar este mensaje explícitamente o mediante la macro [**ICSetState.**](/windows/desktop/api/Vfw/nf-vfw-icsetstate)


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Puntero a un bloque de memoria que contiene datos de configuración. Puede especificar **NULL para** este parámetro a fin de restablecer el estado predeterminado del objeto.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Tamaño, en bytes, del bloque de memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes usados por el resalte si es correcto o cero en caso contrario.

## <a name="remarks"></a>Comentarios

La información utilizada por este mensaje es privada y específica de un determinado resalte. Las aplicaciones cliente solo deben usar este mensaje para restaurar la información obtenida anteriormente con el mensaje [**\_ GETSTATE**](icm-getstate.md) de ICM y deben usar el mensaje [**\_ ICM CONFIGURE**](icm-configure.md) para ajustar la configuración de un controlador de compresión de vídeo.

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

 

 





