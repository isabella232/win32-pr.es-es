---
title: MCIWNDM_PUT_SOURCE mensaje (Vfw.h)
description: El mensaje PUT SOURCE de MCIWNDM redefine las coordenadas del rectángulo de origen usado para recortar las imágenes de un \_ archivo AVI durante la \_ reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c21e11142a1b47a8984712de664151b686cfa3c3cb9bf153dcbc2a23fa459c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807785"
---
# <a name="mciwndm_put_source-message"></a>Mensaje PUT SOURCE de MCIWNDM \_ \_

El **mensaje PUT \_ \_ SOURCE de MCIWNDM** redefine las coordenadas del rectángulo de origen usado para recortar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndPutSource.**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource)


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Prc*
</dt> <dd>

Puntero a una [estructura RECT](/previous-versions//ms536136(v=vs.85)) que contiene las coordenadas del rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

