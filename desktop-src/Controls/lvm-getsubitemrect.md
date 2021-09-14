---
title: LVM_GETSUBITEMRECT mensaje (Commctrl.h)
description: Recupera información sobre el rectángulo delimitador de un subelemento en un control de vista de lista.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974081"
---
# <a name="lvm_getsubitemrect-message"></a>Mensaje \_ GETSUBITEMRECT de LVM

Recupera información sobre el rectángulo delimitador de un subelemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recomendado). Este mensaje está pensado para usarse solo con controles de vista de lista que usan el [**estilo LVS \_ REPORT.**](list-view-window-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento primario del subelemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del rectángulo delimitador de subelemento. Sus miembros se deben inicializar según las siguientes relaciones miembro-valor:



| Value                                                                                                                             | Significado                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>    | Índice basado en uno del subelemento.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**izquierda**</dt> </dl> | Valor de marca (vea comentarios). Indica la parte del subelemento de vista de lista para el que se va a recuperar el rectángulo delimitador.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Estos son los valores de marca que se pueden establecer.



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Valor de marca** | **Significado**                                                                                                         |
| LÍMITES DE LVIR \_   | Devuelve el rectángulo delimitador de todo el elemento, incluidos el icono y la etiqueta.                                    |
| ICONO \_ DE LVIR     | Devuelve el rectángulo delimitador del icono o icono pequeño.                                                           |
| ETIQUETA \_ LVIR    | Devuelve el rectángulo delimitador de todo el elemento, incluidos el icono y la etiqueta. Esto es idéntico a LVIR \_ BOUNDS. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

