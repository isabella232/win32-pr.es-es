---
description: El análisis de diseño funciona en una colección Strokes y clasifica los trazos en elementos de escritura a mano y dibujo. El objeto Divider proporciona acceso a las características de análisis de diseño de Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Análisis de diseño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8131859dd7e4c7bd6927db42bd605541001ac0f1222bfbf27b0e59809d4b7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934825"
---
# <a name="layout-analysis"></a>Análisis de diseño

El análisis de diseño funciona en una [**colección Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) y clasifica los trazos en elementos de escritura a mano y dibujo. El [**objeto Divider**](inkdivider-class.md) proporciona acceso a las características de análisis de diseño de Tablet PC.

En la tabla siguiente se describen los tipos de elementos estructurales de la [**enumeración InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) en la que el objeto [**Divider**](inkdivider-class.md) clasifica los trazos.



| Tipo          | Descripción                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segmento**   | Segmento de reconocimiento.<br/>                                                |
| **Línea**      | Línea de escritura a mano que contiene uno o varios segmentos de reconocimiento.<br/> |
| **Paragraph** | Bloque de trazos que contiene una o varias líneas de escritura a mano.<br/>    |
| **Dibujo**   | Entrada manuscrita que no es de escritura a mano.<br/>                                          |



 

El [**objeto Divider**](inkdivider-class.md) tiene una [**colección Strokes,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el objeto **Divider** analiza dinámicamente cada vez que agrega o elimina de la colección. El **objeto Divider** no es serializable y no se puede guardar su estado de análisis. Por lo tanto, el objeto **Divider** está diseñado para aplicaciones que deben diferenciar entre la escritura a mano mixta y la entrada de dibujo, pero no necesitan volver aanalizar grandes cantidades de entrada de lápiz entre sesiones.

Puede obtener una instantánea estática del resultado del análisis actual, que se devuelve en un [**objeto DivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) Puede obtener objetos [**DivisionUnit,**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) cada uno de los cuales representa un único elemento estructural de un **objeto DivisionResult.** Los **objetos DivisionResult** **y DivisionUnit** no son serializables. Sin embargo, la información de estado de estos objetos está disponible.

El [**objeto Divider**](inkdivider-class.md) solo funciona con escritura a mano de izquierda a derecha. Para que **el objeto Divider** analice correctamente idiomas verticales como el chino, los caracteres se deben dibujar de izquierda a derecha en lugar de de arriba abajo.

 

