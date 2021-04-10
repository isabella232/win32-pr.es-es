---
title: Mensajes que se comunican a través de interfaces de usuario
description: En este tema se enumeran los mensajes que un servicio de directorio puede enviar desde una interfaz de usuario.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Mensajes que se comunican a través de interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075116"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="a034a-104">Mensajes que se comunican a través de interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="a034a-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="a034a-105">En este tema se enumeran los mensajes que un servicio de directorio puede enviar desde una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a034a-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="a034a-106">Mensajes de página de consulta comunes</span><span class="sxs-lookup"><span data-stu-id="a034a-106">Common Query Page Messages</span></span>

<span data-ttu-id="a034a-107">Los siguientes mensajes se envían a una página de extensión de formulario de consulta de servicio de directorio en la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :</span><span class="sxs-lookup"><span data-stu-id="a034a-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="a034a-108">**CQPM \_ CLEARFORM**</span><span class="sxs-lookup"><span data-stu-id="a034a-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="a034a-109">**\_habilitación de CQPM**</span><span class="sxs-lookup"><span data-stu-id="a034a-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="a034a-110">**CQPM \_ GETPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="a034a-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="a034a-111">**CQPM \_ HANDLERSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="a034a-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="a034a-112">**ayuda de CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="a034a-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="a034a-113">**CQPM \_ inicializar**</span><span class="sxs-lookup"><span data-stu-id="a034a-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="a034a-114">**CQPM \_ Persist**</span><span class="sxs-lookup"><span data-stu-id="a034a-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="a034a-115">**versión de CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="a034a-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="a034a-116">**CQPM \_ SETDEFAULTPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="a034a-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="a034a-117">Mensajes varios</span><span class="sxs-lookup"><span data-stu-id="a034a-117">Miscellaneous Messages</span></span>

<span data-ttu-id="a034a-118">En la tabla siguiente se enumeran los mensajes que puede enviar un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="a034a-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="a034a-119">Message</span><span class="sxs-lookup"><span data-stu-id="a034a-119">Message</span></span>                  | <span data-ttu-id="a034a-120">Value</span><span class="sxs-lookup"><span data-stu-id="a034a-120">Value</span></span>                     | <span data-ttu-id="a034a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a034a-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a034a-122">ATTRCHANGED de DSPROP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a034a-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="a034a-123">"DsPropAttrChanged"</span><span class="sxs-lookup"><span data-stu-id="a034a-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="a034a-124">Mensaje enviado para sincronizar las páginas de propiedades y las herramientas de administración del servicio de directorio, declaradas en DSClient. h.</span><span class="sxs-lookup"><span data-stu-id="a034a-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="a034a-125">DSQPM \_ GETCLASSLIST</span><span class="sxs-lookup"><span data-stu-id="a034a-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="a034a-126">CQPM \_ HANDLERSPECIFIC + 0</span><span class="sxs-lookup"><span data-stu-id="a034a-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="a034a-127">Un mensaje de página enviado a las páginas del formulario para recuperar una lista de clases para la consulta, utilizada por el selector de campos y la propiedad bien para generar la lista de clases para mostrar.</span><span class="sxs-lookup"><span data-stu-id="a034a-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="a034a-128">wParam = Flags e lParam = LPLPDSQUERYCLASSLIST, declarado en dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="a034a-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="a034a-129">DSQPM \_ HELPTOPICS</span><span class="sxs-lookup"><span data-stu-id="a034a-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="a034a-130">(CQPM \_ HANDLERSPECIFIC + 1)</span><span class="sxs-lookup"><span data-stu-id="a034a-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="a034a-131">Un mensaje de página enviado a las páginas del formulario para controlar la solicitud de "temas de ayuda".</span><span class="sxs-lookup"><span data-stu-id="a034a-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="a034a-132">wParam = 0, lParam = hWndParent, declarado en dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="a034a-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




