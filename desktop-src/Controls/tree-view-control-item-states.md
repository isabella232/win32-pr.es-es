---
title: Tree-View Estados de elemento de control (CommCtrl. h)
description: En esta sección se enumeran las marcas de estado del elemento que se usan para indicar el estado de un elemento en un control de vista de árbol.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660427"
---
# <a name="tree-view-control-item-states"></a>Estados de los elementos de control Tree-View

En esta sección se enumeran las marcas de estado del elemento que se usan para indicar el estado de un elemento en un control de vista de árbol.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ negrita**</dt> </dl>                               | El elemento está en negrita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**TVIS \_ cortar**</dt> </dl>                                  | El elemento se selecciona como parte de una operación de cortar y pegar. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**TVIS \_ DROPHILITED**</dt> </dl>          | El elemento se selecciona como destino de arrastrar y colocar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**TVIS \_ expandido**</dt> </dl>                   | La lista de elementos secundarios del elemento está expandida actualmente; es decir, los elementos secundarios son visibles. Este valor solo se aplica a los elementos primarios.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**TVIS \_ EXPANDEDONCE**</dt> </dl>       | La lista de elementos secundarios del elemento se ha expandido al menos una vez. Los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) no se generan para los elementos primarios que tienen este estado establecido en respuesta a un mensaje de [**\_ expansión TVM**](tvm-expand.md) . El uso de TVE \_ Collapse y TVE \_ COLLAPSERESET con **TVM \_ Expand** hará que se restablezca este estado. Este valor solo se aplica a los elementos primarios. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**TVIS \_ EXPANDPARTIAL**</dt> </dl>    | **Versión 4,70**. Un elemento de vista de árbol parcialmente expandido. En este estado, algunos, pero no todos, de los elementos secundarios son visibles y se muestra el símbolo más del elemento primario. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS \_ seleccionado**</dt> </dl>                   | El elemento está seleccionado. Su apariencia depende de si tiene el foco. El elemento se dibujará con los colores del sistema para la selección. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**TVIS \_ OVERLAYMASK**</dt> </dl>          | Máscara para los bits que se usan para especificar el índice de imagen de superposición del elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**TVIS \_ STATEIMAGEMASK**</dt> </dl> | Máscara para los bits que se usan para especificar el índice de imagen de estado del elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**TVIS \_ USERMASK**</dt> </dl>                   | Igual que **TVIS \_ STATEIMAGEMASK**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Observaciones

Al establecer o recuperar el índice de imagen de superposición de un elemento o el índice de imagen de estado, debe especificar las siguientes máscaras en el miembro **stateMask** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :

-   **TVIS \_ OVERLAYMASK**
-   **TVIS \_ STATEIMAGEMASK**
-   **TVIS \_ USERMASK**

Estos valores también se pueden usar para enmascarar los bits de estado que no son de interés.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





