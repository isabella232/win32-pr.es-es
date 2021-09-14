---
title: WM_ASKCBFORMATNAME mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles para solicitar el nombre de un formato de Portapapeles \_ OWNERDISPLAY de CF.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME mensaje Data Exchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063876"
---
# <a name="wm_askcbformatname-message"></a>Mensaje \_ ASKCBFORMATNAME de WM

Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles para solicitar el nombre de un formato [**de Portapapeles \_ OWNERDISPLAY de CF.**](standard-clipboard-formats.md)

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en caracteres, del búfer al que apunta el *parámetro lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que va a recibir el nombre de formato del Portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

En respuesta a este mensaje, el propietario del Portapapeles debe copiar el nombre del formato de presentación del propietario en el búfer especificado, sin superar el tamaño de búfer especificado por el *parámetro wParam.*

Una ventana del visor del Portapapeles envía este mensaje al propietario del Portapapeles para determinar el nombre del formato [**\_ OWNERDISPLAY**](standard-clipboard-formats.md) de CF, por ejemplo, para inicializar un menú que enumera los formatos disponibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre el Portapapeles](clipboard.md)
</dt> </dl>

 

