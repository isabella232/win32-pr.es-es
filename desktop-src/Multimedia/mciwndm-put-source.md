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
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250791"
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



 

