---
description: El método GetSPRM recupera el registro de parámetros del sistema especificado.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Método GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997646"
---
# <a name="getsprm-method"></a><span data-ttu-id="2f995-103">Método GetSPRM</span><span class="sxs-lookup"><span data-stu-id="2f995-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="2f995-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2f995-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2f995-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="2f995-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2f995-106">El `GetSPRM` método recupera el registro de parámetros del sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="2f995-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="2f995-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f995-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f995-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="2f995-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="2f995-109">Especifica el registro cuyo valor se desea recuperar como un entero.</span><span class="sxs-lookup"><span data-stu-id="2f995-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="2f995-110">El entero debe oscilar entre 0 y 23.</span><span class="sxs-lookup"><span data-stu-id="2f995-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f995-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f995-111">Return Value</span></span>

<span data-ttu-id="2f995-112">Devuelve un valor entero que representa el contenido del registro especificado.</span><span class="sxs-lookup"><span data-stu-id="2f995-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f995-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f995-113">Remarks</span></span>

<span data-ttu-id="2f995-114">Los registros de parámetros del sistema de controles de disco (SPRMs).</span><span class="sxs-lookup"><span data-stu-id="2f995-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="2f995-115">Una aplicación de reproducción no necesita tener acceso a estos registros para ninguna funcionalidad de navegación estándar.</span><span class="sxs-lookup"><span data-stu-id="2f995-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="2f995-116">SPRMs representa el estado del reproductor.</span><span class="sxs-lookup"><span data-stu-id="2f995-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="2f995-117">Cada una tiene un significado, establecido por las preferencias del usuario, los comandos del disco y otras repeticiones en las que una aplicación no tiene control directo.</span><span class="sxs-lookup"><span data-stu-id="2f995-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="2f995-118">Una aplicación puede leer estos registros, pero no puede escribir en ellos.</span><span class="sxs-lookup"><span data-stu-id="2f995-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="2f995-119">Para usar estos registros de forma eficaz, es probable que necesite un conocimiento más detallado de los comandos de navegación de DVD que los que se proporcionan en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="2f995-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="2f995-120">En la tabla siguiente se muestra el contenido de cada registro.</span><span class="sxs-lookup"><span data-stu-id="2f995-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="2f995-121">Para obtener información más detallada sobre el contenido del registro, vea [ **IDvdInfo2:: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="2f995-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="2f995-122">Register</span><span class="sxs-lookup"><span data-stu-id="2f995-122">Register</span></span> | <span data-ttu-id="2f995-123">Contenido</span><span class="sxs-lookup"><span data-stu-id="2f995-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="2f995-124">0</span><span class="sxs-lookup"><span data-stu-id="2f995-124">0</span></span>        | <span data-ttu-id="2f995-125">Código de idioma del menú</span><span class="sxs-lookup"><span data-stu-id="2f995-125">Menu language code</span></span>              |
| <span data-ttu-id="2f995-126">1</span><span class="sxs-lookup"><span data-stu-id="2f995-126">1</span></span>        | <span data-ttu-id="2f995-127">Número de secuencia de audio</span><span class="sxs-lookup"><span data-stu-id="2f995-127">Audio stream number</span></span>             |
| <span data-ttu-id="2f995-128">2</span><span class="sxs-lookup"><span data-stu-id="2f995-128">2</span></span>        | <span data-ttu-id="2f995-129">Número de secuencia de subimagen</span><span class="sxs-lookup"><span data-stu-id="2f995-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="2f995-130">3</span><span class="sxs-lookup"><span data-stu-id="2f995-130">3</span></span>        | <span data-ttu-id="2f995-131">Número de ángulo actual</span><span class="sxs-lookup"><span data-stu-id="2f995-131">Current angle number</span></span>            |
| <span data-ttu-id="2f995-132">4</span><span class="sxs-lookup"><span data-stu-id="2f995-132">4</span></span>        | <span data-ttu-id="2f995-133">Número de título actual</span><span class="sxs-lookup"><span data-stu-id="2f995-133">Current title number</span></span>            |
| <span data-ttu-id="2f995-134">5</span><span class="sxs-lookup"><span data-stu-id="2f995-134">5</span></span>        | <span data-ttu-id="2f995-135">Número de título</span><span class="sxs-lookup"><span data-stu-id="2f995-135">Title number</span></span>                    |
| <span data-ttu-id="2f995-136">6</span><span class="sxs-lookup"><span data-stu-id="2f995-136">6</span></span>        | <span data-ttu-id="2f995-137">Número de PGC</span><span class="sxs-lookup"><span data-stu-id="2f995-137">PGC number</span></span>                      |
| <span data-ttu-id="2f995-138">7</span><span class="sxs-lookup"><span data-stu-id="2f995-138">7</span></span>        | <span data-ttu-id="2f995-139">Número de capítulo actual (PTT)</span><span class="sxs-lookup"><span data-stu-id="2f995-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="2f995-140">8</span><span class="sxs-lookup"><span data-stu-id="2f995-140">8</span></span>        | <span data-ttu-id="2f995-141">Número de botón resaltado</span><span class="sxs-lookup"><span data-stu-id="2f995-141">Highlighted button number</span></span>       |
| <span data-ttu-id="2f995-142">9</span><span class="sxs-lookup"><span data-stu-id="2f995-142">9</span></span>        | <span data-ttu-id="2f995-143">Temporizador de navegación</span><span class="sxs-lookup"><span data-stu-id="2f995-143">Navigation timer</span></span>                |
| <span data-ttu-id="2f995-144">10</span><span class="sxs-lookup"><span data-stu-id="2f995-144">10</span></span>       | <span data-ttu-id="2f995-145">Salto de PGC para NAV.</span><span class="sxs-lookup"><span data-stu-id="2f995-145">PGC jump for nav.</span></span> <span data-ttu-id="2f995-146">timer</span><span class="sxs-lookup"><span data-stu-id="2f995-146">timer</span></span>         |
| <span data-ttu-id="2f995-147">11</span><span class="sxs-lookup"><span data-stu-id="2f995-147">11</span></span>       | <span data-ttu-id="2f995-148">Modo de presentación de audio de karaoke</span><span class="sxs-lookup"><span data-stu-id="2f995-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="2f995-149">12</span><span class="sxs-lookup"><span data-stu-id="2f995-149">12</span></span>       | <span data-ttu-id="2f995-150">Código de país o región de PML</span><span class="sxs-lookup"><span data-stu-id="2f995-150">PML country/region code</span></span>         |
| <span data-ttu-id="2f995-151">13</span><span class="sxs-lookup"><span data-stu-id="2f995-151">13</span></span>       | <span data-ttu-id="2f995-152">PML</span><span class="sxs-lookup"><span data-stu-id="2f995-152">PML</span></span>                             |
| <span data-ttu-id="2f995-153">14</span><span class="sxs-lookup"><span data-stu-id="2f995-153">14</span></span>       | <span data-ttu-id="2f995-154">Configuración de vídeo</span><span class="sxs-lookup"><span data-stu-id="2f995-154">Video setting</span></span>                   |
| <span data-ttu-id="2f995-155">15</span><span class="sxs-lookup"><span data-stu-id="2f995-155">15</span></span>       | <span data-ttu-id="2f995-156">Funcionalidad de audio</span><span class="sxs-lookup"><span data-stu-id="2f995-156">Audio capability</span></span>                |
| <span data-ttu-id="2f995-157">16</span><span class="sxs-lookup"><span data-stu-id="2f995-157">16</span></span>       | <span data-ttu-id="2f995-158">Idioma de audio</span><span class="sxs-lookup"><span data-stu-id="2f995-158">Audio language</span></span>                  |
| <span data-ttu-id="2f995-159">17</span><span class="sxs-lookup"><span data-stu-id="2f995-159">17</span></span>       | <span data-ttu-id="2f995-160">Extensión de lenguaje de audio</span><span class="sxs-lookup"><span data-stu-id="2f995-160">Audio language extension</span></span>        |
| <span data-ttu-id="2f995-161">18</span><span class="sxs-lookup"><span data-stu-id="2f995-161">18</span></span>       | <span data-ttu-id="2f995-162">Idioma de subimagen</span><span class="sxs-lookup"><span data-stu-id="2f995-162">Subpicture language</span></span>             |
| <span data-ttu-id="2f995-163">19</span><span class="sxs-lookup"><span data-stu-id="2f995-163">19</span></span>       | <span data-ttu-id="2f995-164">Extensión de lenguaje de subimagen</span><span class="sxs-lookup"><span data-stu-id="2f995-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="2f995-165">20</span><span class="sxs-lookup"><span data-stu-id="2f995-165">20</span></span>       | <span data-ttu-id="2f995-166">Código de región del reproductor</span><span class="sxs-lookup"><span data-stu-id="2f995-166">Player region code</span></span>              |
| <span data-ttu-id="2f995-167">21</span><span class="sxs-lookup"><span data-stu-id="2f995-167">21</span></span>       | <span data-ttu-id="2f995-168">Reservado</span><span class="sxs-lookup"><span data-stu-id="2f995-168">Reserved</span></span>                        |
| <span data-ttu-id="2f995-169">22</span><span class="sxs-lookup"><span data-stu-id="2f995-169">22</span></span>       | <span data-ttu-id="2f995-170">Reservado</span><span class="sxs-lookup"><span data-stu-id="2f995-170">Reserved</span></span>                        |
| <span data-ttu-id="2f995-171">23</span><span class="sxs-lookup"><span data-stu-id="2f995-171">23</span></span>       | <span data-ttu-id="2f995-172">Reservado</span><span class="sxs-lookup"><span data-stu-id="2f995-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="2f995-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f995-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f995-174">**GetGPRM**</span><span class="sxs-lookup"><span data-stu-id="2f995-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="2f995-175">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="2f995-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



