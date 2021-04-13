---
title: Mensaje de MCIWNDM_SETZOOM (VFW. h)
description: El \_ mensaje MCIWNDM SETZOOM cambia el tamaño de una imagen de vídeo según un factor de zoom. Este marco ajusta el tamaño de una ventana de MCIWnd mientras mantiene una relación de aspecto constante. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- Mensaje de MCIWNDM_SETZOOM de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489407"
---
# <a name="mciwndm_setzoom-message"></a>MCIWNDM \_ SETZOOM

El mensaje **MCIWNDM \_ SETZOOM** cambia el tamaño de una imagen de vídeo según un factor de zoom. Este marco ajusta el tamaño de una ventana de MCIWnd mientras mantiene una relación de aspecto constante. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

Factor de zoom expresado como porcentaje de la imagen original. Especifique 100 para mostrar la imagen en su tamaño creado, 200 para mostrar la imagen con el doble de tamaño normal, o 50 para mostrar la imagen a la mitad del tamaño normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





