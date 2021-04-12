---
title: Objeto PlayerApplication
description: El objeto PlayerApplication proporciona una manera de coordinar el cambio entre un control de Windows Media Player remoto y el modo completo de Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Objeto PlayerApplication Media Player de Windows
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358341"
---
# <a name="playerapplication-object"></a><span data-ttu-id="f440e-104">Objeto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="f440e-104">PlayerApplication Object</span></span>

<span data-ttu-id="f440e-105">El objeto **PlayerApplication** proporciona una manera de coordinar el cambio entre un control de Windows Media Player remoto y el modo completo de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f440e-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="f440e-106">Este objeto solo se usa con programas de C++ que implementan la interfaz **IWMPRemoteMediaServices** e incrustan el control Player en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="f440e-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="f440e-107">Los archivos de máscara usados como interfaces personalizadas para el control remoto de Windows Media Player tienen acceso a este objeto en el código de script a través del atributo global **playerApplication** .</span><span class="sxs-lookup"><span data-stu-id="f440e-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="f440e-108">El objeto **PlayerApplication** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="f440e-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="f440e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f440e-109">Property</span></span>                                           | <span data-ttu-id="f440e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f440e-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f440e-111">hasDisplay</span><span class="sxs-lookup"><span data-stu-id="f440e-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="f440e-112">Recupera un valor que indica si el vídeo puede mostrarse a través del control remoto de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f440e-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="f440e-113">playerDocked</span><span class="sxs-lookup"><span data-stu-id="f440e-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="f440e-114">Recupera un valor que indica si el Media Player de Windows está en un estado acoplado.</span><span class="sxs-lookup"><span data-stu-id="f440e-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="f440e-115">El objeto **PlayerApplication** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="f440e-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="f440e-116">Método</span><span class="sxs-lookup"><span data-stu-id="f440e-116">Method</span></span>                                                                       | <span data-ttu-id="f440e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f440e-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f440e-118">switchToControl</span><span class="sxs-lookup"><span data-stu-id="f440e-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="f440e-119">Cambia un control de Windows Media Player remoto al estado acoplado.</span><span class="sxs-lookup"><span data-stu-id="f440e-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="f440e-120">switchToPlayerApplication</span><span class="sxs-lookup"><span data-stu-id="f440e-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="f440e-121">Cambia un control de Windows Media Player remoto al modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="f440e-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="f440e-122">Se tiene acceso al objeto **PlayerApplication** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="f440e-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="f440e-123">Object</span><span class="sxs-lookup"><span data-stu-id="f440e-123">Object</span></span>                      | <span data-ttu-id="f440e-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f440e-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="f440e-125">Reproductor</span><span class="sxs-lookup"><span data-stu-id="f440e-125">Player</span></span>](player-object.md) | [<span data-ttu-id="f440e-126">playerApplication</span><span class="sxs-lookup"><span data-stu-id="f440e-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="f440e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f440e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f440e-128">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="f440e-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="f440e-129">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f440e-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




