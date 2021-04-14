---
description: Cómo registrar filtros de DirectShow
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: Cómo registrar filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422874"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="01b51-103">Cómo registrar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="01b51-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="01b51-104">En este artículo se describe cómo hacer que un filtro de Microsoft DirectShow se registre automáticamente.</span><span class="sxs-lookup"><span data-stu-id="01b51-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="01b51-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="01b51-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="01b51-106">Diseño de las claves del registro</span><span class="sxs-lookup"><span data-stu-id="01b51-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="01b51-107">Declarar información de filtro</span><span class="sxs-lookup"><span data-stu-id="01b51-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="01b51-108">Declaración de la plantilla de fábrica</span><span class="sxs-lookup"><span data-stu-id="01b51-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="01b51-109">Implementación de DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="01b51-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="01b51-110">Directrices para registrar filtros</span><span class="sxs-lookup"><span data-stu-id="01b51-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="01b51-111">Anulación del registro de un filtro</span><span class="sxs-lookup"><span data-stu-id="01b51-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="01b51-112">En este artículo no se describe cómo crear un archivo DLL para un filtro de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01b51-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="01b51-113">Para obtener información sobre cómo crear archivos dll, consulte [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="01b51-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01b51-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01b51-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01b51-115">DirectShow y COM</span><span class="sxs-lookup"><span data-stu-id="01b51-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



