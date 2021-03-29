---
title: Interpretar la información de enlace
description: Microsoft RPC permite que los programas de cliente y servidor tengan acceso a la información de un controlador de enlace e la interprete.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- RPC llamada a procedimiento remoto, tareas, interpretar enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487030"
---
# <a name="interpreting-binding-information"></a><span data-ttu-id="656af-104">Interpretar la información de enlace</span><span class="sxs-lookup"><span data-stu-id="656af-104">Interpreting Binding Information</span></span>

<span data-ttu-id="656af-105">Microsoft RPC permite que los programas de cliente y servidor tengan acceso a la información de un controlador de enlace e la interprete.</span><span class="sxs-lookup"><span data-stu-id="656af-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="656af-106">Esto no significa que pueda o debe intentar acceder al contenido de un identificador de enlace directamente.</span><span class="sxs-lookup"><span data-stu-id="656af-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="656af-107">Microsoft RPC proporciona funciones que establecen y recuperan la información en los identificadores de enlace.</span><span class="sxs-lookup"><span data-stu-id="656af-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="656af-108">Para obtener la información de un controlador de enlace, pase el identificador a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="656af-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="656af-109">Devuelve la información de enlace como una cadena.</span><span class="sxs-lookup"><span data-stu-id="656af-109">It returns the binding information as a string.</span></span> <span data-ttu-id="656af-110">Para cada llamada a **RpcBindingToStringBinding**, debe tener una llamada correspondiente a la función [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span><span class="sxs-lookup"><span data-stu-id="656af-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="656af-111">Puede llamar a la función [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para analizar la cadena que obtiene de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="656af-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="656af-112">Esta función asigna cadenas para que contengan la información que analiza.</span><span class="sxs-lookup"><span data-stu-id="656af-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="656af-113">Si no desea que analice una parte determinada de la información de enlace, pase un valor **null** como valor de ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="656af-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="656af-114">Asegúrese de llamar a [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para cada una de las cadenas que asigna.</span><span class="sxs-lookup"><span data-stu-id="656af-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="656af-115">En el fragmento de código siguiente se muestra cómo una aplicación puede llamar a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="656af-115">The following code fragment illustrates how an application might call these functions.</span></span>


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



<span data-ttu-id="656af-116">En el código de ejemplo anterior se llama a las funciones [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) y [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para obtener y analizar la información de un identificador de enlace válido.</span><span class="sxs-lookup"><span data-stu-id="656af-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="656af-117">Tenga en cuenta que el valor **null** se pasó como segundo parámetro a **RpcStringBindingParse**.</span><span class="sxs-lookup"><span data-stu-id="656af-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="656af-118">Esto hace que la función omita el análisis del UUID del objeto.</span><span class="sxs-lookup"><span data-stu-id="656af-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="656af-119">Dado que no analiza el UUID, **RpcStringBindingParse** no asignará una cadena para él.</span><span class="sxs-lookup"><span data-stu-id="656af-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="656af-120">Esta técnica permite que la aplicación solo asigne memoria para la información que le interesa analizar y analizar.</span><span class="sxs-lookup"><span data-stu-id="656af-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 




