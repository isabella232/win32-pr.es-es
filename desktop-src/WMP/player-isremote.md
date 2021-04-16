---
title: Player. isRemote
description: La propiedad isRemote recupera un valor que indica si el control de Media Player de Windows se está ejecutando en modo remoto.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Media Player de Windows Player. isRemote
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649625"
---
# <a name="playerisremote"></a><span data-ttu-id="e9dc2-104">Player. isRemote</span><span class="sxs-lookup"><span data-stu-id="e9dc2-104">Player.isRemote</span></span>

<span data-ttu-id="e9dc2-105">La propiedad **isRemote** recupera un valor que indica si el control de Media Player de Windows se está ejecutando en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="e9dc2-105">The **isRemote** property retrieves a value indicating whether the Windows Media Player control is running in remote mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9dc2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9dc2-106">Syntax</span></span>

<span data-ttu-id="e9dc2-107">*reproductor* . **isRemote**</span><span class="sxs-lookup"><span data-stu-id="e9dc2-107">*player* .**isRemote**</span></span>

## <a name="possible-values"></a><span data-ttu-id="e9dc2-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e9dc2-108">Possible Values</span></span>

<span data-ttu-id="e9dc2-109">Esta propiedad es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9dc2-109">This property is a read-only **Boolean**.</span></span>



| <span data-ttu-id="e9dc2-110">Value</span><span class="sxs-lookup"><span data-stu-id="e9dc2-110">Value</span></span> | <span data-ttu-id="e9dc2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9dc2-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="e9dc2-112">true</span><span class="sxs-lookup"><span data-stu-id="e9dc2-112">true</span></span>  | <span data-ttu-id="e9dc2-113">El control Player se está ejecutando en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="e9dc2-113">The Player control is running in remote mode.</span></span> |
| <span data-ttu-id="e9dc2-114">false</span><span class="sxs-lookup"><span data-stu-id="e9dc2-114">false</span></span> | <span data-ttu-id="e9dc2-115">El control Player se ejecuta en modo local.</span><span class="sxs-lookup"><span data-stu-id="e9dc2-115">The Player control is running in local mode.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="e9dc2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9dc2-116">Remarks</span></span>

<span data-ttu-id="e9dc2-117">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve false.</span><span class="sxs-lookup"><span data-stu-id="e9dc2-117">**Windows Media Player 10 Mobile:** This property always returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9dc2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9dc2-118">Requirements</span></span>



| <span data-ttu-id="e9dc2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9dc2-119">Requirement</span></span> | <span data-ttu-id="e9dc2-120">Value</span><span class="sxs-lookup"><span data-stu-id="e9dc2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dc2-121">Versión</span><span class="sxs-lookup"><span data-stu-id="e9dc2-121">Version</span></span><br/> | <span data-ttu-id="e9dc2-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9dc2-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e9dc2-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9dc2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9dc2-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc2-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9dc2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9dc2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dc2-126">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="e9dc2-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="e9dc2-127">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e9dc2-127">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





