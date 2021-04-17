---
title: Mensaje de ICM_SETSTATE (VFW. h)
description: El \_ mensaje de ICM SETSTATE informa a un controlador de compresión de vídeo para establecer el estado del compresor. Puede enviar este mensaje explícitamente o mediante la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- Mensaje de ICM_SETSTATE de Windows multimedia
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
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677021"
---
# <a name="icm_setstate-message"></a>Mensaje de ICM \_ SETSTATE

El mensaje de **ICM \_ SETSTATE** informa a un controlador de compresión de vídeo para establecer el estado del compresor. Puede enviar este mensaje explícitamente o mediante la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*FV*
</dt> <dd>

Puntero a un bloque de memoria que contiene datos de configuración. Puede especificar **null** para este parámetro a fin de restablecer el compresor a su estado predeterminado.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Tamaño, en bytes, del bloque de memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes utilizados por el compresor si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

La información que usa este mensaje es privada y específica de un compresor determinado. Las aplicaciones cliente deben usar este mensaje solo para restaurar la información obtenida previamente con el mensaje [**\_ GETSTATE ICM**](icm-getstate.md) y deben usar el mensaje de [**\_ configuración de ICM**](icm-configure.md) para ajustar la configuración de un controlador de compresión de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





