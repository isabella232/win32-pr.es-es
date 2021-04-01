---
title: Mensaje de LVM_SORTITEMS (commctrl. h)
description: Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la \_ macro SortItems de ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997189"
---
# <a name="lvm_sortitems-message"></a>\_Mensaje SORTITEMS LVM

Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor definido por la aplicación que se pasa a la función de comparación.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la función de comparación definida por la aplicación. La función de comparación se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La función de comparación tiene el formato siguiente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

El parámetro *lParam1* es el valor asociado al primer elemento que se está comparando y el parámetro *lParam2* es el valor asociado al segundo elemento. Estos son los valores que se especificaron en el miembro **lParam** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de los elementos cuando se insertaron en la lista. El parámetro *wParam* de [**\_ SortItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)se pasa a la función de devolución de llamada como tercer parámetro.

La función de comparación debe devolver un valor negativo si el primer elemento debe preceder al segundo, un valor positivo si el primer elemento debe seguir el segundo, o cero si los dos elementos son equivalentes.

> [!Note]  
> Durante el proceso de ordenación, el contenido de la vista de lista es inestable. Si la función de devolución de llamada envía mensajes al control de vista de lista, aparte del [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), los resultados son imprevisibles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





