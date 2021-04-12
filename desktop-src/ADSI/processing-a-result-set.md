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
# <a name="processing-a-result-set"></a><span data-ttu-id="090a9-103">Procesar un conjunto de resultados</span><span class="sxs-lookup"><span data-stu-id="090a9-103">Processing a Result Set</span></span>

<span data-ttu-id="090a9-104">Un conjunto de resultados se devuelve como una serie de filas.</span><span class="sxs-lookup"><span data-stu-id="090a9-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="090a9-105">Cada fila puede contener o no un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="090a9-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="090a9-106">Con el proveedor de OLE DB, el conjunto de resultados es similar a un conjunto de resultados de SQL normal.</span><span class="sxs-lookup"><span data-stu-id="090a9-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="090a9-107">Si utiliza ADO para la consulta, el [ADODB. ](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) El objeto de conjunto de registros se usa para recorrer el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="090a9-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="090a9-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponible solo desde lenguajes que admiten enlaces vtable) contiene miembros para mover el cursor de fila y comprobar los valores de propiedad en una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="090a9-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="090a9-109">Como alternativa, puede usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para obtener y establecer propiedades.</span><span class="sxs-lookup"><span data-stu-id="090a9-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 