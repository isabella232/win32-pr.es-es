---
title: Ejemplo de diagnósticos NDF
description: En el ejemplo siguiente se muestra cómo iniciar la interfaz de usuario NDF y diagnosticar la conectividad con el sitio web http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075582"
---
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="95cd7-103">Ejemplo de diagnósticos NDF</span><span class="sxs-lookup"><span data-stu-id="95cd7-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="95cd7-104">En el ejemplo siguiente se muestra cómo iniciar la interfaz de usuario NDF y diagnosticar la conectividad con el sitio Web https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="95cd7-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



<span data-ttu-id="95cd7-105">La interfaz de usuario NDF se puede iniciar como una ventana modal.</span><span class="sxs-lookup"><span data-stu-id="95cd7-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="95cd7-106">Para ello, cambie el segundo parámetro de [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) de **null** al identificador (HWND) de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="95cd7-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="95cd7-107">Este ejemplo se puede modificar para diagnosticar otras áreas de redes.</span><span class="sxs-lookup"><span data-stu-id="95cd7-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="95cd7-108">Para ello, reemplace la llamada [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) por una de las otras funciones de creación de incidentes, como [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) o [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span><span class="sxs-lookup"><span data-stu-id="95cd7-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95cd7-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95cd7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95cd7-110">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="95cd7-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="95cd7-111">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="95cd7-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="95cd7-112">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="95cd7-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




