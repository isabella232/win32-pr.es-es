---
description: En la tabla siguiente se muestran los distintos métodos que la aplicación puede usar para controlar el identificador, la justificación y los clústeres.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Trabajar con relaciones entre las posiciones del centro de referencia, los puntos de justificación y los clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069800"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Trabajar con relaciones entre las posiciones del centro de referencia, los puntos de justificación y los clústeres

En la tabla siguiente se muestran los distintos métodos que la aplicación puede usar para controlar el identificador, la justificación y los clústeres.



| Tarea                             | Compatibilidad con Uniscribe                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Movimiento del carácter por clúster de caracteres  | El *parámetro pwLogClust* de la [**función ScriptShapeEl**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) **miembro fClusterStart** de la [**estructura SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> El **miembro fCharStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Separación de línea entre caracteres | El *parámetro pwLogClust* de la [**función ScriptShapeEl**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) **miembro fClusterStart** de la [**estructura SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> El **miembro fCharStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Movimiento del centro de atención por palabra               | El **miembro fWordStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Separación de línea entre palabras      | El **miembro fWordStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Justificación                    | Miembro **uJustification de** la [**estructura SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




