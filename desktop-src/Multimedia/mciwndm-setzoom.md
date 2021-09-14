---
title: MCIWNDM_SETZOOM mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ SETZOOM cambia el tamaño de una imagen de vídeo según un factor de zoom. Este marco ajusta el tamaño de una ventana de MCIWnd mientras se mantiene una relación de aspecto constante. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074220"
---
# <a name="mciwndm_setzoom-message"></a>Mensaje SETZOOM de MCIWNDM \_

El **mensaje MCIWNDM \_ SETZOOM** cambia el tamaño de una imagen de vídeo según un factor de zoom. Este marco ajusta el tamaño de una ventana de MCIWnd mientras se mantiene una relación de aspecto constante. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*Izoom*
</dt> <dd>

Factor de zoom expresado como porcentaje de la imagen original. Especifique 100 para mostrar la imagen en su tamaño de creación, 200 para mostrar la imagen con el doble de su tamaño normal o 50 para mostrar la imagen a la mitad de su tamaño normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





