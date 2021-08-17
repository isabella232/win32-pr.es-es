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
ms.openlocfilehash: 0e8deb133559332ea8f727758086e19cb17483b4c343f8b3f8f1a3694911eedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832273"
---
# <a name="cb_seteditsel-message"></a>Mensaje \_ DE CB SETEDITSEL

Una aplicación envía un mensaje **\_ CB SETEDITSEL** para seleccionar caracteres en el control de edición de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* especifica la posición inicial. Si **loword es** -1, se quita la selección, si existe.

HiWORD [**de**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) *lParam* especifica la posición final. Si **HIWORD es** -1, se selecciona todo el texto desde la posición inicial hasta el último carácter del control de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es **TRUE.** Si el mensaje se envía a un cuadro combinado con el estilo [**\_ DROPDOWNLIST de CBS,**](combo-box-styles.md) es CB \_ ERR.

## <a name="remarks"></a>Comentarios

Las posiciones están basadas en cero. El primer carácter del control de edición está en la posición cero. El primer carácter después del último carácter seleccionado está en la posición final. Por ejemplo, para seleccionar los cuatro primeros caracteres del control de edición, use una posición inicial de 0 y una posición final de 4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETEDITSEL**](cb-geteditsel.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

