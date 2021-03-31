---
title: Mensaje de LVM_SETICONSPACING (commctrl. h)
description: Establece el espaciado entre los iconos de los controles de vista de lista que tienen el estilo de icono de LVS \_ . Puede enviar este mensaje explícitamente o mediante la \_ macro SetIconSpacing de ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING controles de mensajes de Windows
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
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905004"
---
# <a name="lvm_seticonspacing-message"></a>\_Mensaje SETICONSPACING LVM

Establece el espaciado entre los iconos de los controles de vista de lista que tienen el estilo de [**\_ icono de LVS**](list-view-window-styles.md) . Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetIconSpacing de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la distancia, en píxeles, que se va a establecer entre los iconos del eje x. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la distancia, en píxeles, que se va a establecer entre los iconos del eje y. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene la distancia del eje x anterior en la palabra baja y la distancia del eje y anterior en la palabra alta.

## <a name="remarks"></a>Observaciones

Los valores de *lParam* son relativos a la esquina superior izquierda de un mapa de bits de icono. Por lo tanto, para establecer el espaciado entre los iconos que no se superponen, los valores *lParam* deben incluir el tamaño del icono, más la cantidad de espacio vacío deseado entre los iconos. Los valores que no incluyen el ancho del icono darán lugar a superposiciones.

Al definir el espaciado de los iconos, los valores *lParam* deben establecerse en 4 o más. Los valores más pequeños no producirán el diseño deseado. Para restablecer los iconos en el espaciado predeterminado, establezca los valores de *lParam* en-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

