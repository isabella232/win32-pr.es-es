---
title: Procesamiento de un conjunto de resultados
description: Un conjunto de resultados se devuelve como una serie de filas.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174602"
---
# <a name="processing-a-result-set"></a>Procesamiento de un conjunto de resultados

Un conjunto de resultados se devuelve como una serie de filas. Cada fila puede contener o no un atributo determinado. Con el OLE DB de resultados, el conjunto de resultados es similar a un conjunto de resultados SQL normal. Si usa ADO para la consulta, [ADODB. El](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) objeto de conjunto de registros se usa para recorrer el conjunto de resultados. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponible solo desde lenguajes que admiten enlaces de vtable) contiene miembros para mover el cursor de fila y comprobar los valores de propiedad de una fila determinada. Como alternativa, puede usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para obtener y establecer propiedades.

 

 