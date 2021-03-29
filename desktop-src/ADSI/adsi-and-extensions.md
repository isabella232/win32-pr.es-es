---
title: Cómo integra ADSI Extensions
description: Instrucciones que describen cómo interactúa ADSI con las extensiones.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- ADSI de extensiones
- ADSI y extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078365"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="834fc-105">Cómo integra ADSI Extensions</span><span class="sxs-lookup"><span data-stu-id="834fc-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="834fc-106">Las instrucciones siguientes describen cómo interactúa ADSI con las extensiones:</span><span class="sxs-lookup"><span data-stu-id="834fc-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="834fc-107">Algo enlaza a un objeto de directorio ADSI.</span><span class="sxs-lookup"><span data-stu-id="834fc-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="834fc-108">Por ejemplo, "LDAP:Rio = Juanpérez, OU = sales, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="834fc-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="834fc-109">ADSI identifica que el objeto está en la clase de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="834fc-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="834fc-110">ADSI realiza una búsqueda en el registro e identifica los CLSID de la extensión para el **usuario**.</span><span class="sxs-lookup"><span data-stu-id="834fc-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="834fc-111">Tenga en cuenta que ADSI almacena en caché estos datos.</span><span class="sxs-lookup"><span data-stu-id="834fc-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="834fc-112">Algo llama al método **QueryInterface** para IID \_ IMyExtension.</span><span class="sxs-lookup"><span data-stu-id="834fc-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="834fc-113">ADSI busca las interfaces asociadas al objeto de **usuario** , comenzando por sus propias interfaces y, a continuación, examinando las interfaces de extensión.</span><span class="sxs-lookup"><span data-stu-id="834fc-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="834fc-114">Si se encuentra una coincidencia, ADSI crea una instancia del componente que admite IID \_ IMyExtension y llama a **QueryInterface** para la extensión.</span><span class="sxs-lookup"><span data-stu-id="834fc-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="834fc-115">Se devuelve la interfaz resultante.</span><span class="sxs-lookup"><span data-stu-id="834fc-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="834fc-116">El usuario usa esta interfaz para llamar a los métodos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="834fc-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="834fc-117">A continuación, el cliente llama a **QueryInterface** para IID \_ IYourExtension, que se encuentra en un componente diferente.</span><span class="sxs-lookup"><span data-stu-id="834fc-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="834fc-118">Este componente delega esta llamada **QueryInterface** en la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del agregador, que resulta ser ADSI propiamente dicha.</span><span class="sxs-lookup"><span data-stu-id="834fc-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="834fc-119">De nuevo, ADSI busca las interfaces y crea la instancia de componente.</span><span class="sxs-lookup"><span data-stu-id="834fc-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 