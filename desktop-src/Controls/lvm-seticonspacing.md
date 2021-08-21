---
title: LVM_SETICONSPACING mensaje (Commctrl.h)
description: Establece el espaciado entre los iconos de los controles de vista de lista que tienen el estilo LVS \_ ICON. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ SetIconSpacing.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5897b0ca6aec7763cc24a0ea538f336e7a2f737f2ddc0e7cb52a2145e570db47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019183"
---
# <a name="lvm_seticonspacing-message"></a>Mensaje \_ SETICONSPACING de LVM

Establece el espaciado entre los iconos de los controles de vista de lista que tienen el estilo [**LVS \_ ICON.**](list-view-window-styles.md) Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetIconSpacing.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica la**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) distancia, en píxeles, que se establecerá entre los iconos del eje X. HIWORD [**especifica la**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) distancia, en píxeles, que se establecerá entre los iconos del eje Y. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene la distancia del eje X anterior en la palabra baja y la distancia del eje Y anterior en la palabra alta.

## <a name="remarks"></a>Comentarios

Los valores *de lParam* son relativos a la esquina superior izquierda de un mapa de bits de icono. Por lo tanto, para establecer el espaciado entre iconos que no se superponen, los valores *lParam* deben incluir el tamaño del icono, además de la cantidad de espacio vacío deseado entre iconos. Los valores que no incluyen el ancho del icono darán lugar a superposiciones.

Al definir el espaciado de icono, los *valores lParam* deben establecerse en 4 o más. Los valores más pequeños no producen el diseño deseado. Para restablecer el espaciado predeterminado de los iconos, establezca los *valores de lParam* en -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

