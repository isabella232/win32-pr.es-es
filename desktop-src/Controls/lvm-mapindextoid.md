---
title: LVM_MAPINDEXTOID mensaje (Commctrl.h)
description: Mapas el índice de un elemento a un identificador único.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974065"
---
# <a name="lvm_mapindextoid-message"></a>Mensaje \_ MAPINDEXTOID de LVM

Mapas el índice de un elemento a un identificador único.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador único.

## <a name="remarks"></a>Observaciones

Los controles de vista de lista realiza un seguimiento interno de los elementos por índice. Esto puede presentar problemas porque los índices pueden cambiar durante la vigencia del control.

El control list-view puede etiquetar un elemento con un identificador cuando se crea el elemento. Puede usar este identificador para garantizar la unidad durante la vigencia del control list-view.

Para identificar de forma única un elemento, tome el índice que se devuelve de una llamada como [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) y llame a **LVM \_ MAPINDEXTOID**. El valor devuelto es un identificador único.

> [!Note]  
> En un entorno multiproceso, el índice solo se garantiza en el subproceso que hospeda el control de vista de lista, no en subprocesos en segundo plano.

 

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

