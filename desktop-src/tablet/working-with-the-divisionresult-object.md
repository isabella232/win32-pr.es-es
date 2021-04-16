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
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="51816-104">Trabajar con el objeto DivisionResult</span><span class="sxs-lookup"><span data-stu-id="51816-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="51816-105">El objeto **DivisionResult** representa una instantánea del análisis del diseño de los trazos que contiene el objeto **divisor** .</span><span class="sxs-lookup"><span data-stu-id="51816-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="51816-106">Contiene la clasificación del trazo y la información de agrupación del análisis de diseño.</span><span class="sxs-lookup"><span data-stu-id="51816-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="51816-107">Puede obtener información del objeto **DivisionResult** mediante el tipo de elemento estructural, como dibujar o líneas de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="51816-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="51816-108">El objeto **DivisionResult** puede persistir después de que se destruya el objeto **divisor** .</span><span class="sxs-lookup"><span data-stu-id="51816-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="51816-109">En Automation, este objeto se denomina objeto de [**interfaz IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="51816-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="51816-110">La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del objeto **DivisionResult** contiene una copia de la colección **Strokes** en el objeto **divisor** en el momento en que se creó el objeto **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="51816-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="51816-111">La enumeración [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define los tipos de elemento estructurales que reconoce el análisis de diseño.</span><span class="sxs-lookup"><span data-stu-id="51816-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="51816-112">El método [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) del objeto **DivisionResult** devuelve una colección **DivisionUnits** que contiene todos los elementos estructurales de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="51816-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="51816-113">Un elemento estructural individual se representa mediante un objeto **DivisionUnit** .</span><span class="sxs-lookup"><span data-stu-id="51816-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="51816-114">Cada vez que se llama al método **ResultByType** , el objeto **DivisionResult** crea una colección **DivisionUnits** .</span><span class="sxs-lookup"><span data-stu-id="51816-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="51816-115">Para obtener más información sobre el objeto **DivisionUnit** , vea [trabajar con el objeto DivisionUnit](working-with-the-divisionunit-object.md).</span><span class="sxs-lookup"><span data-stu-id="51816-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
