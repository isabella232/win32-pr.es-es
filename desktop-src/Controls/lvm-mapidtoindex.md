---
title: LVM_MAPIDTOINDEX mensaje (Commctrl.h)
description: Mapas el identificador de un elemento a un índice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b5380d52f839f28324b808ed0d3304b6c5e2837869e0f0cfc6ab99d8f00b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079875"
---
# <a name="lvm_mapidtoindex-message"></a>Mensaje \_ LVM MAPIDTOINDEX

Mapas el identificador de un elemento a un índice.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador único de un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice más actual.

## <a name="remarks"></a>Comentarios

Los controles de vista de lista realiza un seguimiento interno de los elementos por índice. Esto puede presentar problemas porque los índices pueden cambiar durante la duración del control.

El control list-view puede etiquetar un elemento con un identificador cuando se crea el elemento. Puede usar este identificador para garantizar la unidad durante la vigencia del control list-view.

Para identificar de forma única un elemento, tome el índice que se devuelve de una llamada como [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) y llame a [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). El valor devuelto es un identificador único.

Si necesita el índice de un elemento después de crear un identificador, puede llamar a **LVM \_ MAPIDTOINDEX** con el identificador único y devuelve el índice más actual.

**LVM \_ NO se admite MAPIDTOINDEX** en el [**estilo LVS \_ OWNERDATA.**](list-view-window-styles.md)

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



 

