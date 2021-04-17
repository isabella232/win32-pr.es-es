---
description: El método NotifyParentalLevelChange habilita o deshabilita el control de eventos para los comandos del nivel de administración parental temporal.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Método NotifyParentalLevelChange (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690409"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="39afa-103">Método NotifyParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="39afa-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="39afa-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="39afa-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="39afa-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="39afa-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="39afa-106">El `NotifyParentalLevelChange` método habilita o deshabilita el control de eventos para los comandos del nivel de administración parental temporal.</span><span class="sxs-lookup"><span data-stu-id="39afa-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="39afa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39afa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39afa-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span><span class="sxs-lookup"><span data-stu-id="39afa-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="39afa-109">Especifica un valor booleano que indica si se notifica o no a la aplicación cuando el objeto MSWebDVD encuentra segmentos de vídeo con una clasificación más restrictiva que la clasificación general del disco.</span><span class="sxs-lookup"><span data-stu-id="39afa-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39afa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39afa-110">Return Value</span></span>

<span data-ttu-id="39afa-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="39afa-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39afa-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39afa-112">Remarks</span></span>

<span data-ttu-id="39afa-113">Las notificaciones de administración parental están deshabilitadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39afa-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="39afa-114">Esto significa que se permiten los comandos parentales temporales del disco, pero se omiten y el disco se reproducirá sin interrupción.</span><span class="sxs-lookup"><span data-stu-id="39afa-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="39afa-115">Llame a este método durante la inicialización de la aplicación si necesita controlar los comandos del nivel de administración parental temporal del disco. Para deshabilitar la administración parental una vez habilitada, llame a este método con un argumento de false.</span><span class="sxs-lookup"><span data-stu-id="39afa-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="39afa-116">Para obtener más información sobre la administración parental, vea [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="39afa-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39afa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39afa-117">Requirements</span></span>



| <span data-ttu-id="39afa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="39afa-118">Requirement</span></span> | <span data-ttu-id="39afa-119">Value</span><span class="sxs-lookup"><span data-stu-id="39afa-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39afa-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39afa-120">Header</span></span><br/> | <dl> <span data-ttu-id="39afa-121"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="39afa-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39afa-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="39afa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39afa-123">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="39afa-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="39afa-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="39afa-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="39afa-125">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="39afa-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="39afa-126">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="39afa-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="39afa-127">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="39afa-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




