---
title: Procesar un conjunto de resultados
description: Un conjunto de resultados se devuelve como una serie de filas.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359412"
---
# <a name="processing-a-result-set"></a>Procesar un conjunto de resultados

Un conjunto de resultados se devuelve como una serie de filas. Cada fila puede contener o no un atributo determinado. Con el proveedor de OLE DB, el conjunto de resultados es similar a un conjunto de resultados de SQL normal. Si utiliza ADO para la consulta, el [ADODB. ](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) El objeto de conjunto de registros se usa para recorrer el conjunto de resultados. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponible solo desde lenguajes que admiten enlaces vtable) contiene miembros para mover el cursor de fila y comprobar los valores de propiedad en una fila determinada. Como alternativa, puede usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para obtener y establecer propiedades.

 

 