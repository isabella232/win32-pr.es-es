---
description: El evento ValidateProductID establece la propiedad ProductID en el identificador de producto completo. Si la validación no se realiza correctamente, este evento coloca un mensaje de error y un cuadro de diálogo modal para una entrada de usuario del ID. de producto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677458"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="4a9fc-104">ValidateProductID ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="4a9fc-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="4a9fc-105">El evento ValidateProductID establece la propiedad [**ProductID**](productid.md) en el identificador de producto completo.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="4a9fc-106">Si la validación no se realiza correctamente, este evento coloca un mensaje de error y un cuadro de diálogo modal para una entrada de usuario del ID. de producto.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="4a9fc-107">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="4a9fc-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="4a9fc-108">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a9fc-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="4a9fc-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9fc-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4a9fc-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4a9fc-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4a9fc-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="4a9fc-112">Publicado por</span><span class="sxs-lookup"><span data-stu-id="4a9fc-112">Published By</span></span>

<span data-ttu-id="4a9fc-113">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="4a9fc-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="4a9fc-114">Argument</span></span>

<span data-ttu-id="4a9fc-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4a9fc-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="4a9fc-116">Action on Subscribers</span></span>

<span data-ttu-id="4a9fc-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4a9fc-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="4a9fc-118">Typical Use</span></span>

<span data-ttu-id="4a9fc-119">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento y se usa para comprobar la entrada del usuario del ID. del producto.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="4a9fc-120">Si la entrada del usuario es válida, se abrirá el siguiente cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



