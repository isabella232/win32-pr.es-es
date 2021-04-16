---
title: Mensaje de LVM_MAPIDTOINDEX (commctrl. h)
description: Asigna el identificador de un elemento a un índice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX controles de mensajes de Windows
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
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658321"
---
# <a name="lvm_mapidtoindex-message"></a>\_Mensaje MAPIDTOINDEX LVM

Asigna el identificador de un elemento a un índice.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

IDENTIFICADOR único de un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice más actual.

## <a name="remarks"></a>Observaciones

Los controles de vista de lista controlan internamente los elementos por índice. Esto puede presentar problemas porque los índices pueden cambiar durante la duración del control.

El control de vista de lista puede etiquetar un elemento con un identificador cuando se crea el elemento. Puede usar este identificador para garantizar la exclusividad durante la duración del control de vista de lista.

Para identificar de forma única un elemento, tome el índice devuelto por una llamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) y llame a [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). El valor devuelto es un identificador único.

Si necesita el índice de un elemento una vez creado un identificador, puede llamar a **LVM \_ MAPIDTOINDEX** con el identificador único y devuelve el índice más actual.

**LVM \_ MAPIDTOINDEX** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

> [!Note]  
> En un entorno multiproceso, el índice solo se garantiza en el subproceso que hospeda el control de vista de lista, no en los subprocesos en segundo plano.

 

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

