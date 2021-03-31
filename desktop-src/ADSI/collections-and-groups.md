---
title: Colecciones y grupos
description: ADSI usa objetos de colección para representar cualquier conjunto arbitrario de elementos de un servicio de directorio que se puede representar con el mismo tipo de datos.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, colecciones y grupos
- ADSI de colecciones
- grupos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995615"
---
# <a name="collections-and-groups"></a><span data-ttu-id="71450-106">Colecciones y grupos</span><span class="sxs-lookup"><span data-stu-id="71450-106">Collections and Groups</span></span>

<span data-ttu-id="71450-107">ADSI usa objetos de colección para representar cualquier conjunto arbitrario de elementos de un servicio de directorio que se puede representar con el mismo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="71450-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="71450-108">Los objetos de colección se definen como un conjunto de valores **Variant** que representan cualquiera de los tipos de datos de automatización válidos.</span><span class="sxs-lookup"><span data-stu-id="71450-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="71450-109">Los objetos de colección pueden representar tanto la información persistente como las listas de control de acceso y la información volátil, como los trabajos de impresión en una cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="71450-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="71450-110">La Convención COM estándar para mostrar el contenido de un objeto de colección (o contenedor) consiste en crear un objeto de enumerador que admita [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), que tiene métodos para recorrer la lista de objetos de colección.</span><span class="sxs-lookup"><span data-stu-id="71450-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="71450-111">Las interfaces de ADSI que proporcionan el método **Get \_ \_ NewEnum** (observe los dos subrayados) son [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) y [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span><span class="sxs-lookup"><span data-stu-id="71450-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="71450-112">ADSI también proporciona las funciones auxiliares [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) y [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) para los programas de C y C++ con el fin de simplificar la enumeración.</span><span class="sxs-lookup"><span data-stu-id="71450-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="71450-113">Los clientes de automatización utilizan la enumeración implícitamente cuando llaman a **Next** en un bucle **for** .</span><span class="sxs-lookup"><span data-stu-id="71450-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="71450-114">Los grupos son simplemente colecciones de objetos que admiten la interfaz [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .</span><span class="sxs-lookup"><span data-stu-id="71450-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 