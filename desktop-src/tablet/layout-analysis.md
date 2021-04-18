---
description: El análisis de diseño funciona en una colección de trazos y clasifica los trazos en elementos de escritura a mano y de dibujo. El objeto divisor proporciona acceso a las características de análisis del diseño de Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Análisis de diseño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720568"
---
# <a name="layout-analysis"></a>Análisis de diseño

El análisis de diseño funciona en una colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) y clasifica los trazos en elementos de escritura a mano y de dibujo. El objeto [**divisor**](inkdivider-class.md) proporciona acceso a las características de análisis del diseño de Tablet PC.

En la tabla siguiente se describen los tipos de elementos estructurales de la enumeración [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) en la que el objeto [**divisor**](inkdivider-class.md) clasifica los trazos.



| Tipo          | Descripción                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segmento**   | Un segmento de reconocimiento.<br/>                                                |
| **Line**      | Línea de escritura a mano que contiene uno o más segmentos de reconocimiento.<br/> |
| **Paragraph** | Bloque de trazos que contiene una o más líneas de escritura a mano.<br/>    |
| **Dibujo**   | Tinta que no es de escritura a mano.<br/>                                          |



 

El objeto [**divisor**](inkdivider-class.md) tiene una colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , que el objeto **divisor** analiza dinámicamente cada vez que se agrega o se elimina de la colección. El objeto **divisor** no es Serializable y no se puede guardar su estado de análisis. Por lo tanto, el objeto **divisor** está diseñado para las aplicaciones que deben diferenciar entre escritura a mano mixta y entrada de dibujo, pero no es necesario volver a analizar grandes cantidades de tinta entre sesiones.

Puede obtener una instantánea estática del resultado del análisis actual, que se devuelve en un objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) . Puede obtener objetos [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , cada uno de los cuales representa un único elemento estructural de un objeto **DivisionResult** . Los objetos **DivisionResult** y **DivisionUnit** no son serializables. Sin embargo, la información de estado de estos objetos está disponible.

El objeto [**divisor**](inkdivider-class.md) funciona solo con escritura a mano de izquierda a derecha. Para que el objeto **divisor** analice los idiomas verticales como el chino correctamente, los caracteres deben dibujarse de izquierda a derecha en lugar de arriba a abajo.

 

