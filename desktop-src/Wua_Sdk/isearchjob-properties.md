---
description: La interfaz ISearchJob define las siguientes propiedades.
ms.assetid: 9e1675e9-fe40-4209-aba9-1cabb4f3ea4c
title: Propiedades de ISearchJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c49a5af7435819750451c89ca68f976d76f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154506"
---
# <a name="isearchjob-properties"></a><span data-ttu-id="31788-103">Propiedades de ISearchJob</span><span class="sxs-lookup"><span data-stu-id="31788-103">ISearchJob Properties</span></span>

<span data-ttu-id="31788-104">La interfaz [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="31788-104">The [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) interface defines the following properties.</span></span>



| <span data-ttu-id="31788-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31788-105">Property</span></span>                                      | <span data-ttu-id="31788-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="31788-106">Description</span></span>                                                                                                                                                 |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31788-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="31788-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_asyncstate)   | <span data-ttu-id="31788-108">Obtiene el objeto de estado específico del llamador que se pasa al método [**IUpdateSearch. BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) .</span><span class="sxs-lookup"><span data-stu-id="31788-108">Gets the caller-specific state object that is passed to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method.</span></span>                         |
| [<span data-ttu-id="31788-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="31788-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_iscompleted) | <span data-ttu-id="31788-110">Obtiene un valor booleano que indica si la llamada al método [**IUpdateSearch. BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) se procesa por completo.</span><span class="sxs-lookup"><span data-stu-id="31788-110">Gets a Boolean value that indicates whether the call to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method is completely processed.</span></span> |



 

 

 



