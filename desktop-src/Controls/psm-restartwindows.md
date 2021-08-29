---
title: PSM_RESTARTWINDOWS mensaje (Prsht.h)
description: Indica que Windows debe reiniciarse para que los cambios suban efecto.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff80191ebed8929a3d7b5079f1bf381ae9ad82ad82c2c177d8f7366e8734dc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877155"
---
# <a name="psm_restartwindows-message"></a>MENSAJE \_ DE REINICIO DE PSMWINDOWS

Indica que Windows debe reiniciarse para que los cambios suban efecto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una aplicación debe enviar este mensaje solo en respuesta al código de notificación [PSN \_ APPLY](psn-apply.md) o [PSN \_ KILLACTIVE.](psn-killactive.md) Puede enviar el mensaje **PSM \_ RESTARTWINDOWS** explícitamente o mediante la [**macro PropSheet \_ RestartWindows.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows)

Este mensaje hace que la función [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el valor \_ de ID PSRESTARTWINDOWS, pero solo si el usuario hace clic en el botón Aceptar para cerrar la hoja de propiedades.  Es responsabilidad de la aplicación reiniciar Windows, lo que se puede hacer mediante la [**función ExitWindowsEx.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

