---
description: PGM usa opciones de socket para establecer el estado, proporcionar parámetros de multidifusión y, de lo contrario, implementar sus capacidades de multidifusión.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opciones de socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907938"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="6c779-103">Opciones de socket PGM</span><span class="sxs-lookup"><span data-stu-id="6c779-103">PGM Socket Options</span></span>

<span data-ttu-id="6c779-104">PGM usa opciones de socket para establecer el estado, proporcionar parámetros de multidifusión y, de lo contrario, implementar sus capacidades de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="6c779-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="6c779-105">En esta página se especifica cómo deben establecerse las opciones de socket PGM, se enumeran las opciones de socket disponibles para PGM y, si es necesario, se proporcionan ejemplos de uso e información adicional para diversas opciones.</span><span class="sxs-lookup"><span data-stu-id="6c779-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="6c779-106">Para ver las definiciones básicas de cada opción de socket PCM, consulte [Opciones de socket](socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="6c779-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="6c779-107">**Windows XP:** No se admite la programación multidifusión confiable (PGM).</span><span class="sxs-lookup"><span data-stu-id="6c779-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="6c779-108">Las siguientes opciones de socket están disponibles para los remitentes de PGM:</span><span class="sxs-lookup"><span data-stu-id="6c779-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="6c779-109">RM \_ LATEJOIN</span><span class="sxs-lookup"><span data-stu-id="6c779-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="6c779-110">tamaño de la ventana de tasa de RM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c779-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="6c779-111">tasa de ADV. de \_ ventana de envío de RM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c779-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="6c779-112">Estadísticas del remitente de RM \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c779-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="6c779-113">\_ \_ \_ método avanzado de la ventana del remitente de RM \_</span><span class="sxs-lookup"><span data-stu-id="6c779-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="6c779-114">RM \_ set \_ MCAST \_ TTL</span><span class="sxs-lookup"><span data-stu-id="6c779-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="6c779-115">\_límite de \_ mensajes de conjunto de RM \_</span><span class="sxs-lookup"><span data-stu-id="6c779-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="6c779-116">RM \_ establecer \_ envío \_ si</span><span class="sxs-lookup"><span data-stu-id="6c779-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="6c779-117">RM \_ usar \_ FEC</span><span class="sxs-lookup"><span data-stu-id="6c779-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="6c779-118">La \_ opción método avanzado de la ventana del remitente de RM \_ \_ \_ especifica el método que se usa al avanzar la ventana de envío del borde final.</span><span class="sxs-lookup"><span data-stu-id="6c779-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="6c779-119">El parámetro optval solo puede ser la \_ ventana E \_ avanzar \_ por \_ tiempo (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="6c779-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="6c779-120">Tenga en cuenta \_ que \_ \_ no se admite la utilización de la ventana en la \_ \_ memoria caché de datos.</span><span class="sxs-lookup"><span data-stu-id="6c779-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="6c779-121">Las siguientes opciones de socket están disponibles para los receptores de PGM:</span><span class="sxs-lookup"><span data-stu-id="6c779-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="6c779-122">\_Agregar recepción de RM \_ \_ si</span><span class="sxs-lookup"><span data-stu-id="6c779-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="6c779-123">RM \_ del \_ receptor \_ si</span><span class="sxs-lookup"><span data-stu-id="6c779-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="6c779-124">RM de \_ alta velocidad de la \_ \_ intranet \_ OPC</span><span class="sxs-lookup"><span data-stu-id="6c779-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="6c779-125">\_estadísticas del receptor de RM \_</span><span class="sxs-lookup"><span data-stu-id="6c779-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="6c779-126">Configuración de las opciones de socket PGM</span><span class="sxs-lookup"><span data-stu-id="6c779-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="6c779-127">En el fragmento de código siguiente se muestra una directriz de programación para establecer las opciones de socket PGM:</span><span class="sxs-lookup"><span data-stu-id="6c779-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="6c779-128">En el fragmento de código anterior, el tipo y el contenido de *OptionData* dependen de la opción de socket que se establece.</span><span class="sxs-lookup"><span data-stu-id="6c779-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="6c779-129">Para todas las opciones de socket PGM, el nivel de socket es IPPROTO \_ RM.</span><span class="sxs-lookup"><span data-stu-id="6c779-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="6c779-130">Las opciones de socket PGM se deben establecer inmediatamente después de la llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) , con las siguientes excepciones:</span><span class="sxs-lookup"><span data-stu-id="6c779-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="6c779-131">\_límite de \_ mensajes de conjunto de RM \_</span><span class="sxs-lookup"><span data-stu-id="6c779-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="6c779-132">Estadísticas del remitente de RM \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c779-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="6c779-133">\_estadísticas del receptor de RM \_</span><span class="sxs-lookup"><span data-stu-id="6c779-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



