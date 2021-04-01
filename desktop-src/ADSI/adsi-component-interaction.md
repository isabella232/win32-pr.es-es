---
title: Interacción de componentes ADSI
description: El componente del enrutador Active Directory rellena una tabla del proveedor ADSI de los proveedores ADSI instalados que aparecen en el registro cuando recibe la primera solicitud de la aplicación cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793804"
---
# <a name="adsi-component-interaction"></a><span data-ttu-id="5a15d-103">Interacción de componentes ADSI</span><span class="sxs-lookup"><span data-stu-id="5a15d-103">ADSI Component Interaction</span></span>

<span data-ttu-id="5a15d-104">El componente del enrutador Active Directory rellena una tabla del proveedor ADSI de los proveedores ADSI instalados que aparecen en el registro cuando recibe la primera solicitud de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5a15d-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="5a15d-105">Para obtener más información sobre el registro, vea [instalar el componente de proveedor de ejemplo](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="5a15d-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="5a15d-106">Las operaciones que realizan una solicitud desde un directorio para un puntero a una interfaz en un objeto Active Directory proceden de una función (**GetObject** en Visual Basic o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) en C o C++) o un método de interfaz ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span><span class="sxs-lookup"><span data-stu-id="5a15d-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="5a15d-107">En la ilustración siguiente, la aplicación cliente ADSI pasa esta solicitud de enlace al componente del enrutador ADSI (1).</span><span class="sxs-lookup"><span data-stu-id="5a15d-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="5a15d-108">El componente router identifica el identificador de programa (ProgID) del proveedor de la primera parte de ADsPath y usa [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para buscar el CLSID coincidente en el registro (2) y carga el componente de proveedor adecuado (3).</span><span class="sxs-lookup"><span data-stu-id="5a15d-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![interacciones de componentes ADSI en el proveedor de ejemplo](images/dscspr.png)

<span data-ttu-id="5a15d-110">En la ilustración anterior, el componente de proveedor crea un objeto Active Directory que representa el elemento de directorio con nombre.</span><span class="sxs-lookup"><span data-stu-id="5a15d-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="5a15d-111">El componente de compatibilidad con ADSI realiza una operación **QueryInterface** en el identificador de interfaz solicitado.</span><span class="sxs-lookup"><span data-stu-id="5a15d-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="5a15d-112">Cuando se recupera un puntero a la interfaz (4), al igual que con todas las implementaciones de cliente/servidor COM, se pasa de nuevo al cliente (5) y, desde ese momento, la aplicación cliente trabaja directamente con el componente de proveedor (6).</span><span class="sxs-lookup"><span data-stu-id="5a15d-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 