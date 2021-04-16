---
description: El objeto DivisionResult representa una instantánea del análisis del diseño de los trazos que contiene el objeto divisor. Contiene la clasificación del trazo y la información de agrupación del análisis de diseño.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Trabajar con el objeto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542542"
---
# <a name="working-with-the-divisionresult-object"></a>Trabajar con el objeto DivisionResult

El objeto **DivisionResult** representa una instantánea del análisis del diseño de los trazos que contiene el objeto **divisor** . Contiene la clasificación del trazo y la información de agrupación del análisis de diseño.

Puede obtener información del objeto **DivisionResult** mediante el tipo de elemento estructural, como dibujar o líneas de escritura a mano. El objeto **DivisionResult** puede persistir después de que se destruya el objeto **divisor** . En Automation, este objeto se denomina objeto de [**interfaz IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del objeto **DivisionResult** contiene una copia de la colección **Strokes** en el objeto **divisor** en el momento en que se creó el objeto **DivisionResult** .

La enumeración [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define los tipos de elemento estructurales que reconoce el análisis de diseño.

El método [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) del objeto **DivisionResult** devuelve una colección **DivisionUnits** que contiene todos los elementos estructurales de un tipo determinado. Un elemento estructural individual se representa mediante un objeto **DivisionUnit** . Cada vez que se llama al método **ResultByType** , el objeto **DivisionResult** crea una colección **DivisionUnits** . Para obtener más información sobre el objeto **DivisionUnit** , vea [trabajar con el objeto DivisionUnit](working-with-the-divisionunit-object.md).

 

 
