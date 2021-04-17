---
description: El método UOPValid recupera un valor que indica si la operación de usuario especificada (UOP) es válida actualmente.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Método UOPValid (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690227"
---
# <a name="uopvalid-method"></a><span data-ttu-id="b9977-103">Método UOPValid</span><span class="sxs-lookup"><span data-stu-id="b9977-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="b9977-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b9977-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b9977-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b9977-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b9977-106">El `UOPValid` método recupera un valor que indica si la operación de usuario especificada (UOP) es válida actualmente.</span><span class="sxs-lookup"><span data-stu-id="b9977-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="b9977-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9977-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9977-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span><span class="sxs-lookup"><span data-stu-id="b9977-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="b9977-109">Especifica la operación de usuario (UOP) como un entero.</span><span class="sxs-lookup"><span data-stu-id="b9977-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="b9977-110">Value</span><span class="sxs-lookup"><span data-stu-id="b9977-110">Value</span></span> | <span data-ttu-id="b9977-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9977-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9977-112">0</span><span class="sxs-lookup"><span data-stu-id="b9977-112">0</span></span>     | <span data-ttu-id="b9977-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="b9977-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="b9977-114">1</span><span class="sxs-lookup"><span data-stu-id="b9977-114">1</span></span>     | [<span data-ttu-id="b9977-115">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="b9977-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="b9977-116">2</span><span class="sxs-lookup"><span data-stu-id="b9977-116">2</span></span>     | [<span data-ttu-id="b9977-117">**PlayTitle**</span><span class="sxs-lookup"><span data-stu-id="b9977-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="b9977-118">3</span><span class="sxs-lookup"><span data-stu-id="b9977-118">3</span></span>     | [<span data-ttu-id="b9977-119">**Stop**</span><span class="sxs-lookup"><span data-stu-id="b9977-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="b9977-120">4</span><span class="sxs-lookup"><span data-stu-id="b9977-120">4</span></span>     | [<span data-ttu-id="b9977-121">**ReturnFromSubmenu**</span><span class="sxs-lookup"><span data-stu-id="b9977-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="b9977-122">5</span><span class="sxs-lookup"><span data-stu-id="b9977-122">5</span></span>     | [<span data-ttu-id="b9977-123">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="b9977-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="b9977-124">6</span><span class="sxs-lookup"><span data-stu-id="b9977-124">6</span></span>     | <span data-ttu-id="b9977-125">[**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="b9977-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="b9977-126">7</span><span class="sxs-lookup"><span data-stu-id="b9977-126">7</span></span>     | [<span data-ttu-id="b9977-127">**PlayNextChapter**</span><span class="sxs-lookup"><span data-stu-id="b9977-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="b9977-128">8</span><span class="sxs-lookup"><span data-stu-id="b9977-128">8</span></span>     | [<span data-ttu-id="b9977-129">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="b9977-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="b9977-130">9</span><span class="sxs-lookup"><span data-stu-id="b9977-130">9</span></span>     | [<span data-ttu-id="b9977-131">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="b9977-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="b9977-132">10</span><span class="sxs-lookup"><span data-stu-id="b9977-132">10</span></span>    | <span data-ttu-id="b9977-133">[**Showmenu**](showmenu-method.md) con un valor de parámetro de 2 ( \_ título de menú de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b9977-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="b9977-134">11</span><span class="sxs-lookup"><span data-stu-id="b9977-134">11</span></span>    | <span data-ttu-id="b9977-135">[**Showmenu**](showmenu-method.md) con un valor de parámetro de 3 ( \_ raíz de menú de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b9977-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="b9977-136">12</span><span class="sxs-lookup"><span data-stu-id="b9977-136">12</span></span>    | <span data-ttu-id="b9977-137">[**Showmenu**](showmenu-method.md) con un valor de parámetro de 4 ( \_ subimagen de menú de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b9977-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="b9977-138">13</span><span class="sxs-lookup"><span data-stu-id="b9977-138">13</span></span>    | <span data-ttu-id="b9977-139">[**Showmenu**](showmenu-method.md) con un valor de parámetro de 5 ( \_ audio de menú de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b9977-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="b9977-140">14</span><span class="sxs-lookup"><span data-stu-id="b9977-140">14</span></span>    | <span data-ttu-id="b9977-141">[**Showmenu**](showmenu-method.md) con un valor de parámetro de 6 ( \_ ángulo de menú de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b9977-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="b9977-142">15</span><span class="sxs-lookup"><span data-stu-id="b9977-142">15</span></span>    | <span data-ttu-id="b9977-143">[**Showmenu**](showmenu-method.md) con un valor de parámetro de 7 ( \_ capítulo de menú de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b9977-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="b9977-144">16</span><span class="sxs-lookup"><span data-stu-id="b9977-144">16</span></span>    | [<span data-ttu-id="b9977-145">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="b9977-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="b9977-146">17</span><span class="sxs-lookup"><span data-stu-id="b9977-146">17</span></span>    | <span data-ttu-id="b9977-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="b9977-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="b9977-148">18</span><span class="sxs-lookup"><span data-stu-id="b9977-148">18</span></span>    | [<span data-ttu-id="b9977-149">**StillOff**</span><span class="sxs-lookup"><span data-stu-id="b9977-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="b9977-150">19</span><span class="sxs-lookup"><span data-stu-id="b9977-150">19</span></span>    | [<span data-ttu-id="b9977-151">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="b9977-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="b9977-152">20</span><span class="sxs-lookup"><span data-stu-id="b9977-152">20</span></span>    | [<span data-ttu-id="b9977-153">**CurrentAudioStream**</span><span class="sxs-lookup"><span data-stu-id="b9977-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="b9977-154">21</span><span class="sxs-lookup"><span data-stu-id="b9977-154">21</span></span>    | [<span data-ttu-id="b9977-155">**CurrentSubpictureStream**</span><span class="sxs-lookup"><span data-stu-id="b9977-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="b9977-156">22</span><span class="sxs-lookup"><span data-stu-id="b9977-156">22</span></span>    | <span data-ttu-id="b9977-157">[**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="b9977-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="b9977-158">23</span><span class="sxs-lookup"><span data-stu-id="b9977-158">23</span></span>    | [<span data-ttu-id="b9977-159">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="b9977-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="b9977-160">24</span><span class="sxs-lookup"><span data-stu-id="b9977-160">24</span></span>    | <span data-ttu-id="b9977-161">Seleccione Preferencias del modo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b9977-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9977-162">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9977-162">Return Value</span></span>

<span data-ttu-id="b9977-163">Devuelve un valor booleano que indica si el control UOP permite la operación especificada.</span><span class="sxs-lookup"><span data-stu-id="b9977-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9977-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9977-164">Requirements</span></span>



| <span data-ttu-id="b9977-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9977-165">Requirement</span></span> | <span data-ttu-id="b9977-166">Value</span><span class="sxs-lookup"><span data-stu-id="b9977-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9977-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9977-167">Header</span></span><br/> | <dl> <span data-ttu-id="b9977-168"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9977-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




