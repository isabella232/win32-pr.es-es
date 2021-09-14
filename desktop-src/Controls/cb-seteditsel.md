---
title: CB_SETEDITSEL mensaje (Winuser.h)
description: Una aplicación envía un mensaje \_ CB SETEDITSEL para seleccionar caracteres en el control de edición de un cuadro combinado.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170114"
---
# <a name="cb_seteditsel-message"></a>Mensaje \_ SETEDITSEL de CB

Una aplicación envía un mensaje **\_ CB SETEDITSEL** para seleccionar caracteres en el control de edición de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* especifica la posición inicial. Si **LOWORD es** -1, se quita la selección, si existe.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* especifica la posición final. Si **HIWORD es** -1, se selecciona todo el texto desde la posición inicial hasta el último carácter del control de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es **TRUE.** Si el mensaje se envía a un cuadro combinado con el estilo [**\_ DROPDOWNLIST de CBS,**](combo-box-styles.md) es CB \_ ERR.

## <a name="remarks"></a>Observaciones

Las posiciones son de base cero. El primer carácter del control de edición está en la posición cero. El primer carácter después del último carácter seleccionado está en la posición final. Por ejemplo, para seleccionar los cuatro primeros caracteres del control de edición, use una posición inicial de 0 y una posición final de 4.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETEDITSEL**](cb-geteditsel.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

