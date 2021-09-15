---
title: MCIWNDM_GET_SOURCE mensaje (Vfw.h)
description: El mensaje GET SOURCE de MCIWNDM recupera las coordenadas del rectángulo de origen usado para recortar las imágenes de un \_ archivo AVI durante la \_ reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476803"
---
# <a name="mciwndm_get_source-message"></a>Mensaje GET SOURCE de MCIWNDM \_ \_

El **mensaje GET \_ \_ SOURCE de MCIWNDM** recupera las coordenadas del rectángulo de origen usado para recortar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetSource.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Prc*
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para contener las coordenadas del rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

