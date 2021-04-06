---
title: Mensaje de LVM_SORTITEMSEX (commctrl. h)
description: Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la \_ macro SortItemsEx de ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078939"
---
# <a name="lvm_sortitemsex-message"></a>\_Mensaje SORTITEMSEX LVM

Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortItemsEx de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor definido por la aplicación que se pasa a la función de comparación.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una función de comparación definida por la aplicación. Se llama a este método durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La función de comparación tiene el formato siguiente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Este mensaje es similar al [**LVM \_ SORTITEMS**](lvm-sortitems.md), excepto para el tipo de información que se pasa a la función de comparación. Con **LVM \_ SORTITEMSEX**, *lParam1* es el índice actual del primer elemento y *lParam2* es el índice actual del segundo elemento. Puede enviar un mensaje [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) para recuperar más información sobre un elemento, si es necesario.

La función de comparación debe devolver un valor negativo si el primer elemento debe preceder al segundo, un valor positivo si el primer elemento debe seguir el segundo, o cero si los dos elementos son equivalentes.

> [!Note]  
> Durante el proceso de ordenación, el contenido de la vista de lista es inestable. Si la función de devolución de llamada envía mensajes al control de vista de lista, aparte del [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), los resultados son imprevisibles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





