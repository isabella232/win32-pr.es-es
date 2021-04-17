---
description: Si una aplicación no desea interferencias fuera de los eventos de una sesión de TAPI o del proveedor de servicios, debe proteger la llamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689546"
---
# <a name="secure-a-session"></a><span data-ttu-id="c9b8b-103">Proteger una sesión</span><span class="sxs-lookup"><span data-stu-id="c9b8b-103">Secure a Session</span></span>

<span data-ttu-id="c9b8b-104">Si una aplicación no desea interferencias fuera de los eventos de una sesión de TAPI o del proveedor de servicios, debe proteger la llamada.</span><span class="sxs-lookup"><span data-stu-id="c9b8b-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="c9b8b-105">Por ejemplo, en un entorno analógico, los tonos en espera pueden destruir una sesión de fax o módem en la llamada original.</span><span class="sxs-lookup"><span data-stu-id="c9b8b-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="c9b8b-106">Una aplicación puede proteger una llamada en el momento en que se realiza la llamada o después de que la llamada ya exista.</span><span class="sxs-lookup"><span data-stu-id="c9b8b-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="c9b8b-107">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="c9b8b-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="c9b8b-108">**TAPI 2. x:** Vea [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span><span class="sxs-lookup"><span data-stu-id="c9b8b-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="c9b8b-109">**TAPI 3. x:** Vea [**ITAddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span><span class="sxs-lookup"><span data-stu-id="c9b8b-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
