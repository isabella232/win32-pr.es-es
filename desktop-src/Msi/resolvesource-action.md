---
description: La acción ResolveSource determina la ubicación del origen y establece la propiedad SourceDir si aún no se ha resuelto el origen.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Acción ResolveSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668357"
---
# <a name="resolvesource-action"></a><span data-ttu-id="a1399-103">Acción ResolveSource</span><span class="sxs-lookup"><span data-stu-id="a1399-103">ResolveSource Action</span></span>

<span data-ttu-id="a1399-104">La acción ResolveSource determina la ubicación del origen y establece la propiedad [**SourceDir**](sourcedir.md) si aún no se ha resuelto el origen.</span><span class="sxs-lookup"><span data-stu-id="a1399-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a1399-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="a1399-105">Sequence Restrictions</span></span>

<span data-ttu-id="a1399-106">La acción ResolveSource debe aparecer después de la [acción CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="a1399-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a1399-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="a1399-107">ActionData Messages</span></span>

<span data-ttu-id="a1399-108">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="a1399-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1399-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1399-109">Remarks</span></span>

<span data-ttu-id="a1399-110">Se debe llamar a la acción ResolveSource antes de usar la propiedad [**SourceDir**](sourcedir.md) en cualquier expresión.</span><span class="sxs-lookup"><span data-stu-id="a1399-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="a1399-111">También se debe llamar a este método antes de intentar recuperar el valor de la propiedad **SourceDir** mediante [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="a1399-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="a1399-112">La acción ResolveSource no debe ejecutarse cuando el origen no está disponible, como puede ser al desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1399-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1399-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1399-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1399-114">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="a1399-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



