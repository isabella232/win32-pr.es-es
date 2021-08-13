---
description: El objeto DivisionResult representa una instantánea del análisis de diseño de los trazos contenidos en el objeto Divider. Contiene la clasificación del trazo y la información de agrupación del análisis de diseño.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Trabajar con el objeto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b1bb001ecc57c0925253b01b129e0c6fcf0c0243c5a77f0eb697e2cc5c618d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715075"
---
# <a name="working-with-the-divisionresult-object"></a>Trabajar con el objeto DivisionResult

El **objeto DivisionResult** representa una instantánea del análisis de diseño de los trazos contenidos en el **objeto Divider.** Contiene la clasificación del trazo y la información de agrupación del análisis de diseño.

Puede obtener información del objeto **DivisionResult** por tipo de elemento estructural, como dibujo o líneas de escritura a mano. El **objeto DivisionResult** puede persistir después **de destruir** el objeto Divider. En Automation, este objeto se denomina objeto [**IInkDivisionResult Interface.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

La [**propiedad Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del **objeto DivisionResult** contiene una copia de la colección **Strokes** del objeto **Divider** en el momento en que se creó el objeto **DivisionResult.**

La [**enumeración InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define los tipos de elementos estructurales que el análisis de diseño reconoce.

El [**método ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) del **objeto DivisionResult** devuelve una colección **DivisionUnits** que contiene todos los elementos estructurales de un tipo determinado. Un elemento estructural individual se representa mediante un **objeto DivisionUnit.** Cada vez que se llama **al método ResultByType,** el **objeto DivisionResult** crea una **colección DivisionUnits.** Para obtener más información sobre el **objeto DivisionUnit,** vea [Trabajar con el objeto DivisionUnit](working-with-the-divisionunit-object.md).

 

 
