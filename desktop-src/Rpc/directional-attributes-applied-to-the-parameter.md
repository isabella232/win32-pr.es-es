---
title: Atributos direccionales aplicados al parámetro
description: Los atributos direccionales \ in \ y \ out \ determinan el modo en que el cliente y el servidor asignan y liberan memoria. En la tabla siguiente se resume el efecto de los atributos direccionales en la asignación de memoria.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676457"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="377cd-104">Atributos direccionales aplicados al parámetro</span><span class="sxs-lookup"><span data-stu-id="377cd-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="377cd-105">Los atributos direccionales \[ [dentro](/windows/desktop/Midl/in) \] y \[ [fuera](/windows/desktop/Midl/out-idl) \] determinan cómo el cliente y el servidor asignan y liberan memoria.</span><span class="sxs-lookup"><span data-stu-id="377cd-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="377cd-106">En la tabla siguiente se resume el efecto de los atributos direccionales en la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="377cd-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="377cd-107">Atributo direccional</span><span class="sxs-lookup"><span data-stu-id="377cd-107">Directional attribute</span></span>    | <span data-ttu-id="377cd-108">Memoria en el cliente</span><span class="sxs-lookup"><span data-stu-id="377cd-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="377cd-109">Memoria en el servidor</span><span class="sxs-lookup"><span data-stu-id="377cd-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="377cd-110">\[[en](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="377cd-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="377cd-111">La aplicación cliente debe asignarse antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="377cd-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="377cd-112">El código auxiliar del servidor asigna.</span><span class="sxs-lookup"><span data-stu-id="377cd-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="377cd-113">\[[fuera](/windows/desktop/Midl/out-idl) de\]</span><span class="sxs-lookup"><span data-stu-id="377cd-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="377cd-114">El código auxiliar del cliente se asigna en la devolución.</span><span class="sxs-lookup"><span data-stu-id="377cd-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="377cd-115">El código auxiliar del servidor asigna solo el puntero de nivel superior; la aplicación de servidor debe asignar todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="377cd-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="377cd-116">El servidor también asigna nuevos datos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="377cd-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="377cd-117">\[**in**, **out**\]</span><span class="sxs-lookup"><span data-stu-id="377cd-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="377cd-118">La aplicación cliente debe asignar los datos iniciales transmitidos al servidor; el código auxiliar de cliente asigna datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="377cd-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="377cd-119">El código auxiliar del servidor asigna los datos iniciales transmitidos desde el cliente; la aplicación de servidor asigna nuevos datos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="377cd-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="377cd-120">En todos estos casos, el código auxiliar de cliente no libera memoria.</span><span class="sxs-lookup"><span data-stu-id="377cd-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="377cd-121">La aplicación cliente debe liberar la memoria antes de que finalice.</span><span class="sxs-lookup"><span data-stu-id="377cd-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="377cd-122">El código auxiliar del servidor libera memoria cuando la llamada a procedimiento remoto devuelve (sujeto al \[ atributo [asignar](/windows/desktop/Midl/allocate) \] ACF).</span><span class="sxs-lookup"><span data-stu-id="377cd-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 