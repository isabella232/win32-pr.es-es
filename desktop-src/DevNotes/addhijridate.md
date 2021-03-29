---
description: '\\Panel de control HKCU \\ internacional.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907070"
---
# <a name="addhijridate"></a><span data-ttu-id="9a325-103">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="9a325-103">AddHijriDate</span></span>

<span data-ttu-id="9a325-104">**\\Panel de control HKCU \\ internacional**</span><span class="sxs-lookup"><span data-stu-id="9a325-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="9a325-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9a325-105">Data type</span></span> | <span data-ttu-id="9a325-106">Intervalo</span><span class="sxs-lookup"><span data-stu-id="9a325-106">Range</span></span>                      | <span data-ttu-id="9a325-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9a325-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="9a325-108">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9a325-108">REG\_SZ</span></span>   | <span data-ttu-id="9a325-109">*Un valor de ajuste válido*</span><span class="sxs-lookup"><span data-stu-id="9a325-109">*A valid adjustment value*</span></span> | <span data-ttu-id="9a325-110">(Ninguna)</span><span class="sxs-lookup"><span data-stu-id="9a325-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="9a325-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a325-111">Description</span></span>

<span data-ttu-id="9a325-112">Especifica ajustes en la fecha en el calendario Hijri.</span><span class="sxs-lookup"><span data-stu-id="9a325-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="9a325-113">El calendario Hijri es un calendario lunar utilizado en el mundo islámico.</span><span class="sxs-lookup"><span data-stu-id="9a325-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="9a325-114">Los meses empiezan y terminan según un decreto que se basa en la observación de la nueva luna.</span><span class="sxs-lookup"><span data-stu-id="9a325-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="9a325-115">Es difícil predecir con precisión el comienzo y el final de los meses, y hay variaciones regionales, por lo que se realiza un ajuste entre cero y dos días en el calendario.</span><span class="sxs-lookup"><span data-stu-id="9a325-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="9a325-116">El valor del registro **AddHijriDate** almacena este valor de ajuste como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a325-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="9a325-117">Value</span><span class="sxs-lookup"><span data-stu-id="9a325-117">Value</span></span>          | <span data-ttu-id="9a325-118">Significado</span><span class="sxs-lookup"><span data-stu-id="9a325-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a325-119">AddHijriDate-2</span><span class="sxs-lookup"><span data-stu-id="9a325-119">AddHijriDate-2</span></span> | <span data-ttu-id="9a325-120">Reste dos días.</span><span class="sxs-lookup"><span data-stu-id="9a325-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="9a325-121">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="9a325-121">AddHijriDate</span></span>   | <span data-ttu-id="9a325-122">Reste un día.</span><span class="sxs-lookup"><span data-stu-id="9a325-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="9a325-123">(en blanco)</span><span class="sxs-lookup"><span data-stu-id="9a325-123">(blank)</span></span>        | <span data-ttu-id="9a325-124">No es necesario realizar ningún ajuste.</span><span class="sxs-lookup"><span data-stu-id="9a325-124">No adjustment is necessary.</span></span> <span data-ttu-id="9a325-125">(Si no se ha ajustado la fecha, esta entrada no aparece en el registro.</span><span class="sxs-lookup"><span data-stu-id="9a325-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="9a325-126">Si la fecha se ha ajustado y se ha restaurado a su valor original, esta entrada aparece en el registro sin valor).</span><span class="sxs-lookup"><span data-stu-id="9a325-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="9a325-127">AddHijriDate + 1</span><span class="sxs-lookup"><span data-stu-id="9a325-127">AddHijriDate+1</span></span> | <span data-ttu-id="9a325-128">Agregue un día.</span><span class="sxs-lookup"><span data-stu-id="9a325-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="9a325-129">AddHijriDate + 2</span><span class="sxs-lookup"><span data-stu-id="9a325-129">AddHijriDate+2</span></span> | <span data-ttu-id="9a325-130">Agregue dos días.</span><span class="sxs-lookup"><span data-stu-id="9a325-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="9a325-131">Esta entrada no existe en el registro de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a325-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="9a325-132">Puede agregarlo mediante el editor del registro Regedit.exe o mediante el método de cambio que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a325-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="9a325-133">Cambiar método</span><span class="sxs-lookup"><span data-stu-id="9a325-133">Change Method</span></span>

<span data-ttu-id="9a325-134">Para cambiar el valor de esta entrada, o para agregarla al registro, primero Instale los archivos para los idiomas de escritura compleja y de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="9a325-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="9a325-135">En el panel de control, haga clic en **configuración regional y de idioma y**, a continuación, haga clic en la pestaña **idiomas** . En **compatibilidad con idioma adicional**, active la casilla para **instalar archivos de idiomas de escritura compleja y de derecha a izquierda (incluido el tailandés)**.</span><span class="sxs-lookup"><span data-stu-id="9a325-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="9a325-136">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a325-136">Click **OK**.</span></span>

<span data-ttu-id="9a325-137">Para cambiar el valor de esta entrada o para agregarla al registro, en el panel de control, haga clic en **Opciones regionales y de idioma**.</span><span class="sxs-lookup"><span data-stu-id="9a325-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="9a325-138">En el campo **estándares y formatos** , seleccione una configuración regional que use el calendario Hijri.</span><span class="sxs-lookup"><span data-stu-id="9a325-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="9a325-139">Haga clic en el botón **personalizar** y, a continuación, haga clic en la pestaña **fecha** . En la lista desplegable **Ajustar fecha Hijri a:** , seleccione el valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="9a325-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="9a325-140">Haga clic en **Aceptar** y en **Aceptar** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="9a325-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="9a325-141">Método de activación</span><span class="sxs-lookup"><span data-stu-id="9a325-141">Activation Method</span></span>

<span data-ttu-id="9a325-142">Los cambios que se realicen en esta entrada a través del panel de control surtirán efecto inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9a325-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



