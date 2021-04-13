---
description: En este tema se definen las constantes de INEG de configuración regional \_ \* utilizadas por NLS.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: Constantes de LOCALE_INEG *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360397"
---
# <a name="locale_ineg-constants"></a><span data-ttu-id="88e07-103">Constantes de INEG de configuración regional \_ \*</span><span class="sxs-lookup"><span data-stu-id="88e07-103">LOCALE\_INEG\* Constants</span></span>

<span data-ttu-id="88e07-104">En este tema se definen las constantes de INEG de configuración regional \_ \* utilizadas por NLS.</span><span class="sxs-lookup"><span data-stu-id="88e07-104">This topic defines the LOCALE\_INEG\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88e07-105">Value</span><span class="sxs-lookup"><span data-stu-id="88e07-105">Value</span></span></th>
<th><span data-ttu-id="88e07-106">Significado</span><span class="sxs-lookup"><span data-stu-id="88e07-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88e07-107">LOCALE_INEGCURR</span><span class="sxs-lookup"><span data-stu-id="88e07-107">LOCALE_INEGCURR</span></span></td>
<td><span data-ttu-id="88e07-108">Modo de moneda negativo.</span><span class="sxs-lookup"><span data-stu-id="88e07-108">Negative currency mode.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88e07-109">Mode</span><span class="sxs-lookup"><span data-stu-id="88e07-109">Mode</span></span></th>
<th><span data-ttu-id="88e07-110">Formato para la moneda negativa</span><span class="sxs-lookup"><span data-stu-id="88e07-110">Format for negative currency</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88e07-111">0</span><span class="sxs-lookup"><span data-stu-id="88e07-111">0</span></span></td>
<td><span data-ttu-id="88e07-112">Paréntesis izquierdo, símbolo monetario, número, paréntesis derecho; por ejemplo, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="88e07-112">Left parenthesis, monetary symbol, number, right parenthesis; for example, ($1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-113">1</span><span class="sxs-lookup"><span data-stu-id="88e07-113">1</span></span></td>
<td><span data-ttu-id="88e07-114">Signo negativo, símbolo de moneda, número; por ejemplo,-$1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-114">Negative sign, monetary symbol, number; for example, -$1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-115">2</span><span class="sxs-lookup"><span data-stu-id="88e07-115">2</span></span></td>
<td><span data-ttu-id="88e07-116">Símbolo de moneda, signo negativo, número; por ejemplo, $-1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-116">Monetary symbol, negative sign, number; for example, $-1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-117">3</span><span class="sxs-lookup"><span data-stu-id="88e07-117">3</span></span></td>
<td><span data-ttu-id="88e07-118">Símbolo monetario, número, signo negativo; por ejemplo, $1,1-</span><span class="sxs-lookup"><span data-stu-id="88e07-118">Monetary symbol, number, negative sign; for example, $1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-119">4</span><span class="sxs-lookup"><span data-stu-id="88e07-119">4</span></span></td>
<td><span data-ttu-id="88e07-120">Paréntesis izquierdo, número, símbolo monetario, paréntesis derecho; por ejemplo, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="88e07-120">Left parenthesis, number, monetary symbol, right parenthesis; for example, (1.1$)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-121">5</span><span class="sxs-lookup"><span data-stu-id="88e07-121">5</span></span></td>
<td><span data-ttu-id="88e07-122">Signo negativo, número, símbolo monetario; por ejemplo,-$1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-122">Negative sign, number, monetary symbol; for example, -1.1$</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-123">6</span><span class="sxs-lookup"><span data-stu-id="88e07-123">6</span></span></td>
<td><span data-ttu-id="88e07-124">Número, signo negativo, símbolo monetario; por ejemplo, 1,1-$</span><span class="sxs-lookup"><span data-stu-id="88e07-124">Number, negative sign, monetary symbol; for example, 1.1-$</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-125">7</span><span class="sxs-lookup"><span data-stu-id="88e07-125">7</span></span></td>
<td><span data-ttu-id="88e07-126">Número, símbolo monetario, signo negativo; por ejemplo, $1,1-</span><span class="sxs-lookup"><span data-stu-id="88e07-126">Number, monetary symbol, negative sign; for example, 1.1$-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-127">8</span><span class="sxs-lookup"><span data-stu-id="88e07-127">8</span></span></td>
<td><span data-ttu-id="88e07-128">Signo negativo, número, espacio, símbolo monetario (como #5, pero con un espacio antes del símbolo monetario); por ejemplo,-$1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-128">Negative sign, number, space, monetary symbol (like #5, but with a space before the monetary symbol); for example, -1.1 $</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-129">9</span><span class="sxs-lookup"><span data-stu-id="88e07-129">9</span></span></td>
<td><span data-ttu-id="88e07-130">Signo negativo, símbolo de moneda, espacio, número (como #1, pero con un espacio después del símbolo monetario); por ejemplo,-$1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-130">Negative sign, monetary symbol, space, number (like #1, but with a space after the monetary symbol); for example, -$ 1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-131">10</span><span class="sxs-lookup"><span data-stu-id="88e07-131">10</span></span></td>
<td><span data-ttu-id="88e07-132">Número, espacio, símbolo monetario, signo negativo (como #7, pero con un espacio antes del símbolo monetario); por ejemplo, $1,1-</span><span class="sxs-lookup"><span data-stu-id="88e07-132">Number, space, monetary symbol, negative sign (like #7, but with a space before the monetary symbol); for example, 1.1 $-</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-133">11</span><span class="sxs-lookup"><span data-stu-id="88e07-133">11</span></span></td>
<td><span data-ttu-id="88e07-134">Símbolo monetario, espacio, número, signo negativo (como #3, pero con un espacio después del símbolo monetario); por ejemplo, $1,1-</span><span class="sxs-lookup"><span data-stu-id="88e07-134">Monetary symbol, space, number, negative sign (like #3, but with a space after the monetary symbol); for example, $ 1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-135">12</span><span class="sxs-lookup"><span data-stu-id="88e07-135">12</span></span></td>
<td><span data-ttu-id="88e07-136">Símbolo monetario, espacio, signo negativo, número (como #2, pero con un espacio después del símbolo monetario); por ejemplo, $-1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-136">Monetary symbol, space, negative sign, number (like #2, but with a space after the monetary symbol); for example, $ -1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-137">13</span><span class="sxs-lookup"><span data-stu-id="88e07-137">13</span></span></td>
<td><span data-ttu-id="88e07-138">Número, signo negativo, espacio, símbolo monetario (como #6, pero con un espacio antes del símbolo monetario); por ejemplo, 1,1-$</span><span class="sxs-lookup"><span data-stu-id="88e07-138">Number, negative sign, space, monetary symbol (like #6, but with a space before the monetary symbol); for example, 1.1- $</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-139">14</span><span class="sxs-lookup"><span data-stu-id="88e07-139">14</span></span></td>
<td><span data-ttu-id="88e07-140">Paréntesis izquierdo, símbolo monetario, espacio, número, paréntesis derecho (como #0, pero con un espacio después del símbolo monetario); por ejemplo, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="88e07-140">Left parenthesis, monetary symbol, space, number, right parenthesis (like #0, but with a space after the monetary symbol); for example, ($ 1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-141">15</span><span class="sxs-lookup"><span data-stu-id="88e07-141">15</span></span></td>
<td><span data-ttu-id="88e07-142">Paréntesis izquierdo, número, espacio, símbolo monetario, paréntesis derecho (como #4, pero con un espacio antes del símbolo monetario); por ejemplo, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="88e07-142">Left parenthesis, number, space, monetary symbol, right parenthesis (like #4, but with a space before the monetary symbol); for example, (1.1 $)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-143">LOCALE_INEGNUMBER</span><span class="sxs-lookup"><span data-stu-id="88e07-143">LOCALE_INEGNUMBER</span></span></td>
<td><span data-ttu-id="88e07-144">Modo de número negativo, es decir, el formato de un número negativo.</span><span class="sxs-lookup"><span data-stu-id="88e07-144">Negative number mode, that is, the format for a negative number.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88e07-145">Value</span><span class="sxs-lookup"><span data-stu-id="88e07-145">Value</span></span></th>
<th><span data-ttu-id="88e07-146">Formato</span><span class="sxs-lookup"><span data-stu-id="88e07-146">Format</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88e07-147">0</span><span class="sxs-lookup"><span data-stu-id="88e07-147">0</span></span></td>
<td><span data-ttu-id="88e07-148">Paréntesis izquierdo, número, paréntesis derecho; por ejemplo, (1,1)</span><span class="sxs-lookup"><span data-stu-id="88e07-148">Left parenthesis, number, right parenthesis; for example, (1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-149">1</span><span class="sxs-lookup"><span data-stu-id="88e07-149">1</span></span></td>
<td><span data-ttu-id="88e07-150">Signo negativo, número; por ejemplo,-1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-150">Negative sign, number; for example, -1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-151">2</span><span class="sxs-lookup"><span data-stu-id="88e07-151">2</span></span></td>
<td><span data-ttu-id="88e07-152">Signo negativo, espacio, número; por ejemplo,-1,1</span><span class="sxs-lookup"><span data-stu-id="88e07-152">Negative sign, space, number; for example, - 1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-153">3</span><span class="sxs-lookup"><span data-stu-id="88e07-153">3</span></span></td>
<td><span data-ttu-id="88e07-154">Número, signo negativo; por ejemplo, 1,1-</span><span class="sxs-lookup"><span data-stu-id="88e07-154">Number, negative sign; for example, 1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-155">4</span><span class="sxs-lookup"><span data-stu-id="88e07-155">4</span></span></td>
<td><span data-ttu-id="88e07-156">Número, espacio, signo negativo; por ejemplo, 1,1-</span><span class="sxs-lookup"><span data-stu-id="88e07-156">Number, space, negative sign; for example, 1.1 -</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-157">LOCALE_INEGSEPBYSPACE</span><span class="sxs-lookup"><span data-stu-id="88e07-157">LOCALE_INEGSEPBYSPACE</span></span></td>
<td><span data-ttu-id="88e07-158">Separación del signo negativo en un valor monetario.</span><span class="sxs-lookup"><span data-stu-id="88e07-158">Separation of the negative sign in a monetary value.</span></span> <span data-ttu-id="88e07-159">Este valor es 1 si el símbolo de moneda está separado por un espacio de la cantidad negativa, o 0 si no lo está.</span><span class="sxs-lookup"><span data-stu-id="88e07-159">This value is 1 if the monetary symbol is separated by a space from the negative amount, or 0 if it is not.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-160">LOCALE_INEGSIGNPOSN</span><span class="sxs-lookup"><span data-stu-id="88e07-160">LOCALE_INEGSIGNPOSN</span></span></td>
<td><span data-ttu-id="88e07-161">Índice de formato para el signo negativo en valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="88e07-161">Formatting index for the negative sign in currency values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88e07-162">Value</span><span class="sxs-lookup"><span data-stu-id="88e07-162">Value</span></span></th>
<th><span data-ttu-id="88e07-163">Significado</span><span class="sxs-lookup"><span data-stu-id="88e07-163">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88e07-164">0</span><span class="sxs-lookup"><span data-stu-id="88e07-164">0</span></span></td>
<td><span data-ttu-id="88e07-165">Los paréntesis rodean la cantidad y el símbolo monetario.</span><span class="sxs-lookup"><span data-stu-id="88e07-165">Parentheses surround the amount and the monetary symbol.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-166">1</span><span class="sxs-lookup"><span data-stu-id="88e07-166">1</span></span></td>
<td><span data-ttu-id="88e07-167">El signo precede al número.</span><span class="sxs-lookup"><span data-stu-id="88e07-167">The sign precedes the number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-168">2</span><span class="sxs-lookup"><span data-stu-id="88e07-168">2</span></span></td>
<td><span data-ttu-id="88e07-169">El signo sigue el número.</span><span class="sxs-lookup"><span data-stu-id="88e07-169">The sign follows the number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88e07-170">3</span><span class="sxs-lookup"><span data-stu-id="88e07-170">3</span></span></td>
<td><span data-ttu-id="88e07-171">El signo precede al símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="88e07-171">The sign precedes the monetary symbol.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-172">4</span><span class="sxs-lookup"><span data-stu-id="88e07-172">4</span></span></td>
<td><span data-ttu-id="88e07-173">El signo sigue el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="88e07-173">The sign follows the monetary symbol.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88e07-174">LOCALE_INEGSYMPRECEDES</span><span class="sxs-lookup"><span data-stu-id="88e07-174">LOCALE_INEGSYMPRECEDES</span></span></td>
<td><span data-ttu-id="88e07-175">Posición del símbolo de moneda en un valor monetario negativo.</span><span class="sxs-lookup"><span data-stu-id="88e07-175">Position of the monetary symbol in a negative monetary value.</span></span> <span data-ttu-id="88e07-176">Este valor es 1 si el símbolo de moneda precede a la cantidad negativa, o 0 si el símbolo sigue a la cantidad.</span><span class="sxs-lookup"><span data-stu-id="88e07-176">This value is 1 if the monetary symbol precedes the negative amount, or 0 if the symbol follows the amount.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



