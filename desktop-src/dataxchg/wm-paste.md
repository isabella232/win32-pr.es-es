---
title: Mensaje de WM_PASTE (Winuser. h)
description: Una aplicación envía un \_ mensaje de pegado de WM a un control de edición o un cuadro combinado para copiar el contenido actual del portapapeles en el control de edición situado en la posición actual del símbolo de intercalación. Los datos se insertan solo si el Portapapeles contiene datos en \_ formato de texto CF.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Intercambio de datos de mensajes de WM_PASTE
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422531"
---
# <a name="wm_paste-message"></a>\_Mensaje de pegado de WM

Una aplicación envía un mensaje de **\_ pegado de WM** a un control de edición o un cuadro combinado para copiar el contenido actual del portapapeles en el control de edición situado en la posición actual del símbolo de intercalación. Los datos se insertan solo si el Portapapeles contiene datos en formato de [**\_ texto CF**](standard-clipboard-formats.md) .


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se envía a un cuadro combinado, el mensaje de **\_ pegado de WM** se controla mediante su control de edición. Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_borrado de WM**](wm-clear.md)
</dt> <dt>

[**copia de WM \_**](wm-copy.md)
</dt> <dt>

[**cortar de WM \_**](wm-cut.md)
</dt> <dt>

[**deshacer de WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

