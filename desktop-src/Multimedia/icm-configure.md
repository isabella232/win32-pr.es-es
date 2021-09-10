---
title: ICM_CONFIGURE mensaje (Vfw.h)
description: El ICM configure notifica a un controlador de compresión de vídeo que muestre su cuadro de diálogo de configuración o consulta a un controlador de compresión de vídeo para determinar si tiene un cuadro de diálogo \_ de configuración.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370436"
---
# <a name="icm_configure-message"></a>\_ICM MENSAJE DE CONFIGURACIÓN

El **ICM \_ configure** notifica a un controlador de compresión de vídeo que muestre su cuadro de diálogo de configuración o consulta a un controlador de compresión de vídeo para determinar si tiene un cuadro de diálogo de configuración. Puede enviar este mensaje explícitamente o mediante la macro [**ICConfigure.**](/windows/desktop/api/Vfw/nf-vfw-icconfigure)


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo mostrado. Puede determinar si un controlador tiene un cuadro de diálogo de configuración especificando 1 en este parámetro, como en la macro [**ICQueryConfigure.**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ UNSUPPORTED en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje es diferente del mensaje [**DRV \_ CONFIGURE**](drv-configure.md) que se usa para la configuración de hardware. El cuadro de diálogo de este mensaje debe permitir que el usuario establezca y edite el estado interno al que hacen referencia los ICM [**\_ GETSTATE**](icm-getstate.md) y [**ICM \_ SETSTATE.**](icm-setstate.md) Por ejemplo, este cuadro de diálogo puede permitir que el usuario cambie los parámetros que afectan al nivel de calidad y a otras opciones de compresión similares.

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

 

 





