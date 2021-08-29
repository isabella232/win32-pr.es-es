---
description: En la tabla siguiente se muestran los distintos métodos que la aplicación puede usar para controlar el caret, la justificación y los clústeres.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Trabajar con relaciones entre posiciones de cursor de referencia, puntos de justificación y clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3272fc7284ff0d3223cf2b36a3b764e273bcec66dadc24cc50bf0393ded9b9ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680865"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Trabajar con relaciones entre posiciones de cursor de referencia, puntos de justificación y clústeres

En la tabla siguiente se muestran los distintos métodos que la aplicación puede usar para controlar el caret, la justificación y los clústeres.



| Tarea                             | Compatibilidad con Unscribe                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Movimiento del carácter de caret por clúster de caracteres  | El *parámetro pwLogClust* de la [**función ScriptShapeEl**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) **miembro fClusterStart** de la [**estructura SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> Miembro **fCharStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Separación de línea entre caracteres | El *parámetro pwLogClust* de la [**función ScriptShapeEl**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) **miembro fClusterStart** de la [**estructura SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> Miembro **fCharStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Movimiento del centro de atención por palabra               | Miembro **fWordStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Separación de línea entre palabras      | Miembro **fWordStop** de la [**estructura \_ LOGATTR de SCRIPT**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Justificación                    | Miembro **uJustification** de la [**estructura SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




