---
description: La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser (acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813643"
---
# <a name="registeruser-action"></a><span data-ttu-id="41c42-103">RegisterUser (acción)</span><span class="sxs-lookup"><span data-stu-id="41c42-103">RegisterUser Action</span></span>

<span data-ttu-id="41c42-104">La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.</span><span class="sxs-lookup"><span data-stu-id="41c42-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="41c42-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="41c42-105">Sequence Restrictions</span></span>

<span data-ttu-id="41c42-106">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="41c42-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="41c42-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="41c42-107">ActionData Messages</span></span>



| <span data-ttu-id="41c42-108">Campo</span><span class="sxs-lookup"><span data-stu-id="41c42-108">Field</span></span> | <span data-ttu-id="41c42-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="41c42-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="41c42-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="41c42-110">\[1\]</span></span> | <span data-ttu-id="41c42-111">Información de usuario registrada.</span><span class="sxs-lookup"><span data-stu-id="41c42-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="41c42-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41c42-112">Remarks</span></span>

<span data-ttu-id="41c42-113">La acción RegisterUser no se realiza durante una instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="41c42-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="41c42-114">Si el identificador de producto especificado por el usuario no se ha validado mediante la [Acción ValidateProductID](validateproductid-action.md), no se establece la propiedad [**ProductID**](productid.md) y esta acción no hace nada.</span><span class="sxs-lookup"><span data-stu-id="41c42-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41c42-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41c42-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41c42-116">**NOMBRE**</span><span class="sxs-lookup"><span data-stu-id="41c42-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="41c42-117">**COMPAÑÍA**</span><span class="sxs-lookup"><span data-stu-id="41c42-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="41c42-118">**IdProducto**</span><span class="sxs-lookup"><span data-stu-id="41c42-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



