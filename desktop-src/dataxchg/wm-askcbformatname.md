---
title: WM_ASKCBFORMATNAME mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles para solicitar el nombre de un formato de Portapapeles \_ CF OWNERDISPLAY.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME mensaje De datos Exchange
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
ms.openlocfilehash: bfe96a2ddf4e6767c083ec2e3f4e3fc61bdde902ff93ce9a162ec7e93eb5bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991245"
---
# <a name="wm_askcbformatname-message"></a>Mensaje \_ ASKCBFORMATNAME de WM

Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles para solicitar el nombre de un formato [**de Portapapeles \_ CF OWNERDISPLAY.**](standard-clipboard-formats.md)

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

## <a name="remarks"></a>Comentarios

En respuesta a este mensaje, el propietario del Portapapeles debe copiar el nombre del formato de presentación del propietario en el búfer especificado, sin superar el tamaño de búfer especificado por el *parámetro wParam.*

Una ventana del visor del Portapapeles envía este mensaje al propietario del Portapapeles para determinar el nombre del formato [**\_ CF OWNERDISPLAY,**](standard-clipboard-formats.md) por ejemplo, para inicializar un menú que muestra los formatos disponibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del Portapapeles](clipboard.md)
</dt> </dl>

 

