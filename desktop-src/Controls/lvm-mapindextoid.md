---
title: LVM_MAPINDEXTOID mensaje (Commctrl.h)
description: Mapas índice de un elemento a un identificador único.
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
ms.openlocfilehash: 254bfff0ee1598b0657b44a967b9e1331b076a462c8703855c5dd23109a8835d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958154"
---
# <a name="lvm_mapindextoid-message"></a>Mensaje \_ MAPINDEXTOID de LVM

Mapas índice de un elemento a un identificador único.

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

## <a name="remarks"></a>Comentarios

Los controles de vista de lista realiza un seguimiento interno de los elementos por índice. Esto puede presentar problemas porque los índices pueden cambiar durante la duración del control.

El control list-view puede etiquetar un elemento con un identificador cuando se crea el elemento. Puede usar este identificador para garantizar la unidad durante la vigencia del control list-view.

Para identificar de forma única un elemento, tome el índice que se devuelve de una llamada como [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) y llame a **LVM \_ MAPINDEXTOID**. El valor devuelto es un identificador único.

> [!Note]  
> En un entorno multiproceso, el índice solo se garantiza en el subproceso que hospeda el control de vista de lista, no en subprocesos en segundo plano.

 

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

