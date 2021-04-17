---
description: Este atributo mide hasta qué punto se rellena la barra del indicador de progreso.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Atributo de control de progreso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653037"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="9c7af-103">Atributo de control de progreso</span><span class="sxs-lookup"><span data-stu-id="9c7af-103">Progress Control Attribute</span></span>

<span data-ttu-id="9c7af-104">Este atributo mide hasta qué punto se rellena la barra del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="9c7af-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="9c7af-105">El registro contiene dos enteros y una cadena.</span><span class="sxs-lookup"><span data-stu-id="9c7af-105">The record contains two integers and a string.</span></span> <span data-ttu-id="9c7af-106">El primer número es el progreso, el segundo número es el intervalo (el número máximo posible para el progreso).</span><span class="sxs-lookup"><span data-stu-id="9c7af-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="9c7af-107">Al establecer, los enteros se pueden especificar como campos de tipo entero o cadenas que contengan los enteros.</span><span class="sxs-lookup"><span data-stu-id="9c7af-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="9c7af-108">Si falta el segundo número, se supone que es el valor predeterminado (1024).</span><span class="sxs-lookup"><span data-stu-id="9c7af-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="9c7af-109">Si el progreso es mayor que el intervalo, se cambia para que sea el intervalo.</span><span class="sxs-lookup"><span data-stu-id="9c7af-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="9c7af-110">El tercer campo es una cadena, el nombre de la acción cuyo progreso se muestra.</span><span class="sxs-lookup"><span data-stu-id="9c7af-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="9c7af-111">Para obtener información relacionada, vea [crear un control ProgressBar](authoring-a-progressbar-control.md)y [Agregar acciones personalizadas a ProgressBar](adding-custom-actions-to-the-progressbar.md).</span><span class="sxs-lookup"><span data-stu-id="9c7af-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="9c7af-112">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="9c7af-112">Valid Controls</span></span>

[<span data-ttu-id="9c7af-113">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="9c7af-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="9c7af-114">Marcas de bits asociadas</span><span class="sxs-lookup"><span data-stu-id="9c7af-114">Associated Bit Flags</span></span>

<span data-ttu-id="9c7af-115">Este atributo no utiliza marcas de bits.</span><span class="sxs-lookup"><span data-stu-id="9c7af-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7af-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c7af-116">Remarks</span></span>

<span data-ttu-id="9c7af-117">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="9c7af-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



