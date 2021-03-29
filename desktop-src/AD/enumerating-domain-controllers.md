---
title: Enumerar controladores de dominio
description: En versiones anteriores de Windows, una aplicación solo podía obtener un único controlador de dominio en un dominio llamando a DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, enumerar controladores de dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773231"
---
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="a5fa1-104">Enumerar controladores de dominio</span><span class="sxs-lookup"><span data-stu-id="a5fa1-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="a5fa1-105">En versiones anteriores de Windows, una aplicación solo podía obtener un único controlador de dominio en un dominio llamando a [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span><span class="sxs-lookup"><span data-stu-id="a5fa1-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="a5fa1-106">No había forma de predecir qué controlador de dominio se recuperaría o para obtener una lista de los controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="a5fa1-107">Windows permite a una aplicación enumerar los controladores de dominio de un dominio mediante las funciones [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)y [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="a5fa1-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="a5fa1-108">Para enumerar un controlador de dominio, llame a [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span><span class="sxs-lookup"><span data-stu-id="a5fa1-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="a5fa1-109">Esta función toma parámetros que definen el dominio que se va a enumerar y otras opciones de enumeración.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="a5fa1-110">**DsGetDcOpen** proporciona un identificador de contexto de enumeración de dominio que se usa para identificar la operación de enumeración cuando se llama a [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) y [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="a5fa1-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="a5fa1-111">Se llama a la función [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) con el identificador de contexto de enumeración de dominio para recuperar el siguiente controlador de dominio en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="a5fa1-112">La primera vez que se llama a esta función, se recupera el primer controlador de dominio de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="a5fa1-113">La segunda vez que se llama a esta función, se recupera el segundo controlador de dominio de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="a5fa1-114">Este proceso se repite hasta que **DsGetDcNext** devuelve el **error \_ no \_ más \_ elementos**, que indica el final de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="a5fa1-115">La función [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) enumerará los controladores de dominio en dos grupos.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="a5fa1-116">El primer grupo contiene los controladores de dominio que cubren el sitio del equipo en el que se ejecuta la función y el segundo grupo contiene los controladores de dominio que no cubren el sitio del equipo en el que se ejecuta la función.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="a5fa1-117">Si se especifica la marca **DS \_ Notify \_ After \_ \_ Records site** en el parámetro *OptionFlags* de [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), la función **DsGetDcNext** devolverá una marca de tiempo de **error \_ \_ detectada** después de que se hayan recuperado todos los controladores de dominio específicos del sitio.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="a5fa1-118">**DsGetDcNext** comenzará a enumerar el segundo grupo, que contiene todos los controladores de dominio del dominio, incluidos los controladores de dominio específicos del sitio contenidos en el primer grupo.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="a5fa1-119">Los controladores de dominio que administran el sitio del equipo en el que se ejecuta la función se enumeran primero seguidos de los controladores de dominio que no cubren el sitio del equipo en el que se ejecuta la función.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="a5fa1-120">Se dice que un controlador de dominio cubre un sitio si el controlador de dominio está configurado para residir en ese sitio o si el controlador de dominio reside en un sitio más cercano al sitio en cuestión en lo que respecta al costo de vínculo configurado entre sitios.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="a5fa1-121">Si hay controladores de dominio en el grupo de controladores de dominio que cubren y el grupo de controladores de dominio que no cubren el sitio del equipo, se devuelven controladores de dominio en el grupo en el orden de las prioridades y pesos configurados que se especifican en DNS.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="a5fa1-122">Los controladores de dominio que tienen una prioridad numérica más baja se devuelven primero dentro de un grupo.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="a5fa1-123">Si en un grupo relacionado con el sitio hay un subgrupo de varios controladores de dominio con la misma prioridad, los controladores de dominio se devuelven en un orden aleatorio ponderado, donde los controladores de dominio con mayor peso tienen más probabilidad de ser devueltos en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="a5fa1-124">El administrador del dominio configura los sitios, las prioridades y los pesos para lograr un rendimiento eficaz y un equilibrio de carga entre varios controladores de dominio disponibles en el dominio.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="a5fa1-125">Por este motivo, las aplicaciones que usan [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)las / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / funciones [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) de DsGetDcNext de DsGetDcOpen aprovechan automáticamente estas optimizaciones.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="a5fa1-126">Cuando la enumeración está completa o ya no es necesaria, la enumeración debe cerrarse llamando a [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) con el identificador de contexto de enumeración de dominio.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="a5fa1-127">Para restablecer la enumeración, es necesario cerrar la enumeración actual llamando a [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) y, a continuación, volver a abrir la enumeración llamando a [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) de nuevo.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="a5fa1-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5fa1-128">Example</span></span>

<span data-ttu-id="a5fa1-129">En el ejemplo de código siguiente se muestra cómo usar estas funciones para enumerar los controladores de dominio del dominio local.</span><span class="sxs-lookup"><span data-stu-id="a5fa1-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




