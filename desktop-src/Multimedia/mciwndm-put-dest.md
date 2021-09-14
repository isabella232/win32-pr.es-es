---
title: MCIWNDM_PUT_DEST mensaje (Vfw.h)
description: El mensaje PUT DEST de MCIWNDM redefine las coordenadas del rectángulo de destino que se usa para acercar o ajustar las imágenes de un \_ archivo AVI durante la \_ reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250796"
---
# <a name="mciwndm_put_dest-message"></a>Mensaje PUT \_ DEST de MCIWNDM \_

El **mensaje PUT \_ \_ DEST de MCIWNDM** redefine las coordenadas del rectángulo de destino que se usa para acercar o ajustar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPutDest.**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Prc*
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas del rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

