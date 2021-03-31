---
title: Mensajes de error extendidos de ADSI
description: Este tema contiene una lista de temas que explican cómo trabajar con mensajes de error ADSI devueltos por IADs, IADsContainer, IDirectoryObject y IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Mensajes de error extendidos de ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075089"
---
# <a name="adsi-extended-error-messages"></a><span data-ttu-id="30113-104">Mensajes de error extendidos de ADSI</span><span class="sxs-lookup"><span data-stu-id="30113-104">ADSI Extended Error Messages</span></span>

<span data-ttu-id="30113-105">Además de los valores **HRESULT** , varios proveedores de sistema ADSI (principalmente LDAP) devuelven datos de error adicionales para las operaciones realizadas por las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="30113-105">Apart from the **HRESULT** values, several ADSI system providers (mostly LDAP) return additional error data for operations performed by the following interfaces:</span></span>

-   [<span data-ttu-id="30113-106">**IADs**</span><span class="sxs-lookup"><span data-stu-id="30113-106">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="30113-107">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="30113-107">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="30113-108">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="30113-108">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="30113-109">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="30113-109">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="30113-110">Una parte de estos datos de error extendidos es la cadena enviada por el servidor como parte del resultado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="30113-110">A part of such extended error data is the string sent by the server as a part of the message result.</span></span>

<span data-ttu-id="30113-111">Llame a [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) para recuperar los mensajes de error extendidos.</span><span class="sxs-lookup"><span data-stu-id="30113-111">Call [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) to retrieve such extended error messages.</span></span> <span data-ttu-id="30113-112">El primer parámetro de esta función, *lpError*, es un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="30113-112">The first parameter of this function, *lpError*, is a **DWORD** value.</span></span> <span data-ttu-id="30113-113">Para un servidor de Active Directory, ADSI intenta asignar un mensaje de error LDAP a un código de error de Win32 adecuado y asigna el valor del código de error de Win32 a *lpError*.</span><span class="sxs-lookup"><span data-stu-id="30113-113">For an Active Directory server, ADSI attempts to map an LDAP error message to an appropriate Win32 error code and assigns the Win32 error code value to *lpError*.</span></span> <span data-ttu-id="30113-114">Si no se resuelve la asignación, ADSI asigna un **error de \_ \_ datos no válidos** a *lpError*, como lo hace para cualquier otro servidor de directorio.</span><span class="sxs-lookup"><span data-stu-id="30113-114">Failing to resolve the mapping, ADSI assigns **ERROR\_INVALID\_DATA** to *lpError*, as it does for any other directory server.</span></span> <span data-ttu-id="30113-115">En todos los casos, ADSI retransmite fielmente la cadena de la descripción del error del servidor al cliente a través de *lpErrorBuf*, el segundo parámetro de la función **ADsGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="30113-115">In all cases, ADSI faithfully relays the string of the error description from the server to the client through *lpErrorBuf*, the second parameter of the **ADsGetLastError** function.</span></span>

 

 




