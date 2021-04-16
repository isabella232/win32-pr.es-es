---
title: List-View Estados de elemento (CommCtrl. h)
description: El valor de estado de un elemento consta del estado del elemento, un índice de máscara de superposición opcional y un índice de máscara de imagen de estado opcional.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649796"
---
# <a name="list-view-item-states"></a>List-View Estados de elemento

El valor de estado de un elemento consta del estado del elemento, un índice de máscara de superposición opcional y un índice de máscara de imagen de estado opcional.

El estado de un elemento determina su apariencia y funcionalidad. El estado puede ser cero o uno o varios de los siguientes valores:



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**activación de LVIS \_**</dt> </dl>             | No se admite actualmente.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ cortar**</dt> </dl>                                  | El elemento está marcado para una operación de cortar y pegar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | El elemento se resalta como un destino de arrastrar y colocar.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ centrado**</dt> </dl>                      | El elemento tiene el foco, por lo que está rodeado por un rectángulo de foco estándar. Aunque se puede seleccionar más de un elemento, solo un elemento puede tener el foco.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Una máscara recupera el índice de la imagen de superposición del elemento.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ seleccionado**</dt> </dl>                   | El elemento está seleccionado. La apariencia de un elemento seleccionado depende de si tiene el foco y también de los colores del sistema utilizados para la selección.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Una máscara recupera el índice de la imagen de estado del elemento.<br/>                                                                                                      |



## <a name="remarks"></a>Observaciones

Puede usar la **LVIS \_ OVERLAYMASK** Mask para aislar el índice basado en uno de la imagen de superposición. Puede usar la máscara **\_ STATEIMAGEMASK de LVIS** para aislar el índice basado en uno de la imagen de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





