---
title: TB_ADDBITMAP mensaje (Commctrl.h)
description: Agrega una o varias imágenes a la lista de imágenes de botón disponibles para una barra de herramientas.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b024c224ab305c4a13942c62a2de8d769d2f23b82d21ef295e024bae82f563
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919235"
---
# <a name="tb_addbitmap-message"></a>Mensaje \_ ADDBITMAP de TB

Agrega una o varias imágenes a la lista de imágenes de botón disponibles para una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de imágenes de botón en el mapa de bits. Si *lParam especifica* un mapa de bits definido por el sistema, se omite este parámetro.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) que contiene el identificador de un recurso de mapa de bits y el identificador de la instancia del módulo con el archivo ejecutable que contiene el recurso de mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la primera imagen nueva si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

Si la barra de herramientas se creó mediante la función [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) debe enviar el mensaje [**\_ TB BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) a la barra de herramientas antes de **enviar TB \_ ADDBITMAP**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un mapa de bits a partir de un recurso (IDB BITMAP1), se asigna el color de fondo (negro en este caso) al color de la cara del botón del sistema y se agrega a la barra de \_ herramientas.


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

