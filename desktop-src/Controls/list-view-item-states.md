---
title: List-View de elementos (CommCtrl.h)
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
ms.openlocfilehash: 9040272afc16f500806a3d7a90a0b062018d2f4dec8510e4abe57b24cbc75e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958394"
---
# <a name="list-view-item-states"></a>List-View de elementos

El valor de estado de un elemento consta del estado del elemento, un índice de máscara de superposición opcional y un índice de máscara de imagen de estado opcional.

El estado de un elemento determina su apariencia y funcionalidad. El estado puede ser cero o uno o varios de los valores siguientes:



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**ACTIVACIÓN DE LVIS \_**</dt> </dl>             | Actualmente no se admite.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | El elemento está marcado para una operación de cortar y pegar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | El elemento se resalta como un destino de arrastrar y colocar.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ CENTRADO**</dt> </dl>                      | El elemento tiene el foco, por lo que está rodeado por un rectángulo de foco estándar. Aunque se puede seleccionar más de un elemento, solo un elemento puede tener el foco.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**SUPERPOSICIÓN \_ DE LVISMASK**</dt> </dl>          | El índice de imagen superpuesta del elemento se recupera mediante una máscara.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECCIONADO**</dt> </dl>                   | El elemento está seleccionado. La apariencia de un elemento seleccionado depende de si tiene el foco y también de los colores del sistema usados para la selección.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | El índice de imagen de estado del elemento se recupera mediante una máscara.<br/>                                                                                                      |



## <a name="remarks"></a>Comentarios

Puede usar la máscara **\_ OVERLAYMASK** de LVIS para aislar el índice basado en uno de la imagen superpuesta. Puede usar la máscara **LVIS \_ STATEIMAGEMASK** para aislar el índice basado en uno de la imagen de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





