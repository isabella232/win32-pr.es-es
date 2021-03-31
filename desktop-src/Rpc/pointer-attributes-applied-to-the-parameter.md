---
title: Atributos de puntero aplicados al parámetro
description: Cada atributo de puntero (\ Ref \, \ Unique \ y \ PTR \) tiene características que afectan a la asignación de memoria. En la tabla siguiente se resumen estas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078199"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="643fc-104">Atributos de puntero aplicados al parámetro</span><span class="sxs-lookup"><span data-stu-id="643fc-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="643fc-105">Cada atributo de puntero ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] y \[ [ptr](/windows/desktop/Midl/ptr) \] ) tiene características que afectan a la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="643fc-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="643fc-106">En la tabla siguiente se resumen estas características.</span><span class="sxs-lookup"><span data-stu-id="643fc-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="643fc-107">Atributo de puntero</span><span class="sxs-lookup"><span data-stu-id="643fc-107">Pointer attribute</span></span>       | <span data-ttu-id="643fc-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="643fc-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="643fc-109">Servidor</span><span class="sxs-lookup"><span data-stu-id="643fc-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="643fc-110">Referencia ( \[ **ref** \] )</span><span class="sxs-lookup"><span data-stu-id="643fc-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="643fc-111">La aplicación cliente debe asignar.</span><span class="sxs-lookup"><span data-stu-id="643fc-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="643fc-112">Control especial necesario para punteros de nivel de nontop de solo **\[ salida \]**.</span><span class="sxs-lookup"><span data-stu-id="643fc-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="643fc-113">Único ( \[ **único** \] )</span><span class="sxs-lookup"><span data-stu-id="643fc-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="643fc-114">Si es un parámetro, la aplicación cliente debe asignar; Si está incrustado, puede ser null.</span><span class="sxs-lookup"><span data-stu-id="643fc-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="643fc-115">Cambiar de null a no NULL hace que el código auxiliar de cliente se asigne; Si se cambia de un valor distinto de null a NULL, se puede producir un huérfano.</span><span class="sxs-lookup"><span data-stu-id="643fc-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="643fc-116">Completo ( \[ **ptr** \] )</span><span class="sxs-lookup"><span data-stu-id="643fc-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="643fc-117">Si es un parámetro, la aplicación cliente debe asignar; Si está incrustado, puede ser null.</span><span class="sxs-lookup"><span data-stu-id="643fc-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="643fc-118">Cambiar de null a no NULL hace que el código auxiliar de cliente se asigne; Si se cambia de un valor distinto de null a NULL, se puede producir un huérfano.</span><span class="sxs-lookup"><span data-stu-id="643fc-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="643fc-119">El atributo **\[ ref \]** indica que el puntero apunta a la memoria válida.</span><span class="sxs-lookup"><span data-stu-id="643fc-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="643fc-120">Por definición, la aplicación cliente debe asignar toda la memoria que requieran los punteros de referencia.</span><span class="sxs-lookup"><span data-stu-id="643fc-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="643fc-121">El puntero único puede cambiar de null a un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="643fc-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="643fc-122">Si el puntero único cambia de null a no NULL, se asignará una nueva memoria en el cliente.</span><span class="sxs-lookup"><span data-stu-id="643fc-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="643fc-123">Si el puntero único cambia de distinto de null a NULL, se puede producir el huérfano.</span><span class="sxs-lookup"><span data-stu-id="643fc-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="643fc-124">Para obtener más información, consulte [memoria huérfana](memory-orphaning.md).</span><span class="sxs-lookup"><span data-stu-id="643fc-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

