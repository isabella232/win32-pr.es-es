---
title: Mensaje de MCIWNDM_GET_SOURCE (VFW. h)
description: El \_ \_ mensaje de origen de MCIWNDM Get recupera las coordenadas del rectángulo de origen utilizado para recortar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- Mensaje de MCIWNDM_GET_SOURCE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422496"
---
# <a name="mciwndm_get_source-message"></a>MCIWNDM \_ obtener \_ mensaje de origen

El mensaje de **\_ \_ origen de MCIWNDM Get** recupera las coordenadas del rectángulo de origen utilizado para recortar las imágenes de un archivo AVI durante la reproducción. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para que contenga las coordenadas del rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

