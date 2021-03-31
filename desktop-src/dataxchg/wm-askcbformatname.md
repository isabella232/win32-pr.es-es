---
title: Mensaje de WM_ASKCBFORMATNAME (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles para solicitar el nombre de un \_ formato de Portapapeles de OWNERDISPLAY de CF.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Intercambio de datos de mensajes de WM_ASKCBFORMATNAME
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150079"
---
# <a name="wm_askcbformatname-message"></a>Mensaje de ASKCBFORMATNAME de WM \_

Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles para solicitar el nombre de un formato de Portapapeles de [**\_ OWNERDISPLAY de CF**](standard-clipboard-formats.md) .

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en caracteres, del búfer al que apunta el parámetro *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que va a recibir el nombre de formato del portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

En respuesta a este mensaje, el propietario del portapapeles debe copiar el nombre del formato de presentación del propietario en el búfer especificado, sin superar el tamaño de búfer especificado por el parámetro *wParam* .

Una ventana del visor del portapapeles envía este mensaje al propietario del portapapeles para determinar el nombre del formato [**\_ OWNERDISPLAY de CF**](standard-clipboard-formats.md) , por ejemplo, para inicializar un menú que muestre los formatos disponibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del portapapeles](clipboard.md)
</dt> </dl>

 

