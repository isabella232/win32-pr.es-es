---
title: MCIWNDM_CHANGESTYLES mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ CHANGESTYLES cambia los estilos usados por la ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES mensaje Windows Multimedia
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
ms.openlocfilehash: 5525066f4c377cc093e1e7a0dedd4edf7463792c136214a519da9744917cbc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525515"
---
# <a name="mciwndm_changestyles-message"></a>Mensaje CHANGESTYLES de MCIWNDM \_

El **mensaje MCIWNDM \_ CHANGESTYLES** cambia los estilos usados por la ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndChangeStyles.**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*Máscara*
</dt> <dd>

Máscara que identifica los estilos que pueden cambiar. Esta máscara es el operador OR bit a bit de todos los estilos que se permitirán cambiar.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valor*
</dt> <dd>

Nueva configuración de estilo para la ventana. Especifique cero para este parámetro para desactivar todos los estilos identificados en la máscara. Para obtener una lista de los estilos disponibles, vea la [**función MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





