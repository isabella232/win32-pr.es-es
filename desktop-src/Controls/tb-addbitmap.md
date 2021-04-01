---
title: Mensaje de TB_ADDBITMAP (commctrl. h)
description: Agrega una o más imágenes a la lista de imágenes de botón disponibles para una barra de herramientas.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP controles de mensajes de Windows
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
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804129"
---
# <a name="tb_addbitmap-message"></a>\_Mensaje ADDBITMAP TB

Agrega una o más imágenes a la lista de imágenes de botón disponibles para una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de imágenes de botón en el mapa de bits. Si *lParam* especifica un mapa de bits definido por el sistema, este parámetro se omite.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) que contiene el identificador de un recurso de mapa de bits y el identificador de la instancia de módulo con el archivo ejecutable que contiene el recurso de mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la primera imagen nueva si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

Si la barra de herramientas se creó mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , debe enviar el mensaje de [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) a la barra de herramientas antes de enviar **TB \_ ADDBITMAP**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un mapa de bits a partir de un recurso (IDB \_ BITMAP1), se asigna el color de fondo (negro en este caso) al color de la superficie del botón del sistema y se agrega a la barra de herramientas.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

