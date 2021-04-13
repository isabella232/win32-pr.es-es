---
title: Enlace en tiempo de ejecución en el capó
description: En este tema se describe cómo funciona el enlace en tiempo de ejecución en ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, enlace en tiempo de ejecución, lo que sucede en el capó
- enlazar AD, enlace en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488275"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="5b8fe-105">Enlace en tiempo de ejecución: ¿Qué está ocurriendo en el capó?</span><span class="sxs-lookup"><span data-stu-id="5b8fe-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="5b8fe-106">En la siguiente lista se describe el proceso general para realizar un enlace en tiempo de ejecución:</span><span class="sxs-lookup"><span data-stu-id="5b8fe-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="5b8fe-107">Algo enlaza a un objeto de directorio ADSI.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="5b8fe-108">Por ejemplo, "LDAP: Fiera = Juanpérez, OU = sales, DC = Fabrikam, DC = COM" enlaza mediante enlace COM en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="5b8fe-109">Esto hace que ADSI llame al método [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en la interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="5b8fe-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="5b8fe-110">ADSI busca un objeto en la clase User y crea un objeto que admite las interfaces adecuadas, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span><span class="sxs-lookup"><span data-stu-id="5b8fe-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="5b8fe-111">ADSI realiza una búsqueda en el registro y busca CLSID de extensión para el usuario.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="5b8fe-112">Tenga en cuenta que ADSI almacena en caché estos datos.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="5b8fe-113">Algo realiza una llamada al método **MyNewMethod** .</span><span class="sxs-lookup"><span data-stu-id="5b8fe-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="5b8fe-114">ADSI busca su identificador de envío y los ID. de envío de otras extensiones ADSI.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="5b8fe-115">ADSI busca la extensión que sirve a esta llamada y llama a la interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para esa extensión.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="5b8fe-116">La extensión ejecuta la función.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-116">The extension executes the function.</span></span>
-   <span data-ttu-id="5b8fe-117">Ahora, el escritor de cliente invoca el método **YourNewMethod** con la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para la extensión actual.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="5b8fe-118">La implementación de **IDispatch** de la extensión delega en **IDispatch** para ADSI.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="5b8fe-119">La interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para ADSI vuelve a buscar la extensión adecuada, o a continuación, llama a la extensión adecuada mediante la interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para esa extensión.</span><span class="sxs-lookup"><span data-stu-id="5b8fe-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 