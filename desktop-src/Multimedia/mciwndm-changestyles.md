---
title: Mensaje de MCIWNDM_CHANGESTYLES (VFW. h)
description: El \_ mensaje MCIWNDM CHANGESTYLES cambia los estilos usados por la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- Mensaje de MCIWNDM_CHANGESTYLES de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651388"
---
# <a name="mciwndm_changestyles-message"></a>MCIWNDM \_ CHANGESTYLES

El mensaje **MCIWNDM \_ CHANGESTYLES** cambia los estilos usados por la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*máscara*
</dt> <dd>

Máscara que identifica los estilos que pueden cambiar. Esta máscara es el operador OR bit a bit de todos los estilos que se permitirán cambiar.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Nueva configuración de estilo para la ventana. Especifique cero para que este parámetro desactive todos los estilos identificados en la máscara. Para obtener una lista de los estilos disponibles, vea la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





