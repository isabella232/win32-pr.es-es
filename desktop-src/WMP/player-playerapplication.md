---
title: Player. playerApplication
description: La propiedad playerApplication recupera el objeto PlayerApplication cuando se está ejecutando un control remoto de Windows Media Player.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Media Player de Windows Player. playerApplication
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708825"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="5b809-104">Player. playerApplication</span><span class="sxs-lookup"><span data-stu-id="5b809-104">Player.playerApplication</span></span>

<span data-ttu-id="5b809-105">La propiedad **playerApplication** recupera el objeto **playerApplication** cuando se está ejecutando un control remoto de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5b809-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b809-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b809-106">Syntax</span></span>

<span data-ttu-id="5b809-107">**playerApplication**</span><span class="sxs-lookup"><span data-stu-id="5b809-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5b809-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5b809-108">Possible Values</span></span>

<span data-ttu-id="5b809-109">Esta propiedad es un objeto **PlayerApplication** de solo lectura o el valor null.</span><span class="sxs-lookup"><span data-stu-id="5b809-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b809-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b809-110">Remarks</span></span>

<span data-ttu-id="5b809-111">Esta propiedad solo se utiliza cuando la comunicación remota de Windows Media Playercontrol.</span><span class="sxs-lookup"><span data-stu-id="5b809-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="5b809-112">Si el valor es null, el Playercontrol de Windows Media no se incrusta en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="5b809-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="5b809-113">Esta propiedad solo es accesible en código de C++ o en código de script en máscaras a través de la variable global playerApplication.</span><span class="sxs-lookup"><span data-stu-id="5b809-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b809-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b809-114">Requirements</span></span>



| <span data-ttu-id="5b809-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b809-115">Requirement</span></span> | <span data-ttu-id="5b809-116">Value</span><span class="sxs-lookup"><span data-stu-id="5b809-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b809-117">Versión</span><span class="sxs-lookup"><span data-stu-id="5b809-117">Version</span></span><br/> | <span data-ttu-id="5b809-118">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="5b809-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5b809-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b809-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b809-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b809-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b809-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b809-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b809-122">**Atributos globales**</span><span class="sxs-lookup"><span data-stu-id="5b809-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b809-123">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="5b809-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="5b809-124">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="5b809-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="5b809-125">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5b809-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





