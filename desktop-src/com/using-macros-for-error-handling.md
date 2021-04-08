---
title: Usar macros para el control de errores
description: COM define una serie de macros que facilitan el trabajo con valores HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793966"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="2a1d1-103">Usar macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="2a1d1-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="2a1d1-104">COM define una serie de macros que facilitan el trabajo con valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a1d1-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="2a1d1-105">Las macros de control de errores se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1d1-106">Macro</span><span class="sxs-lookup"><span data-stu-id="2a1d1-106">Macro</span></span></th>
<th><span data-ttu-id="2a1d1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a1d1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a1d1-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-109">Devuelve un <strong>valor HRESULT</strong> dado el bit de gravedad, el código de la instalación y el código de error que componen el <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2a1d1-110">La llamada a <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> para la comprobación de S_OK conlleva una reducción del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="2a1d1-111">No debe utilizar habitualmente <strong>MAKE_HRESULT</strong> para obtener resultados correctos.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1d1-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-113">Devuelve un <strong>SCODE</strong> dado el bit de gravedad, el código de la instalación y el código de error que componen el <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a1d1-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-115">Extrae la parte del código de error de <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1d1-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-117">Extrae el código de instalación de <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a1d1-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-119">Extrae el bit de gravedad del <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1d1-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-121">Extrae la parte del código de error del <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a1d1-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-123">Extrae el código de instalación del <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1d1-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-125">Extrae el campo de gravedad del <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a1d1-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>COMPLETA</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-127">Comprueba el bit de gravedad del <strong>SCODE</strong> o <strong>HRESULT</strong>; Devuelve <strong>true</strong> si la gravedad es cero y <strong>false</strong> si es uno.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1d1-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>ERRÓNEO</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-129">Comprueba el bit de gravedad del <strong>SCODE</strong> o <strong>HRESULT</strong>; Devuelve <strong>true</strong> si la gravedad es una y <strong>false</strong> si es cero.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a1d1-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-131">Proporciona una prueba genérica de errores en cualquier valor de estado.</span><span class="sxs-lookup"><span data-stu-id="2a1d1-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a1d1-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-133">Asigna un <a href="/windows/desktop/Debug/system-error-codes">código de error del sistema</a> a un valor <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a1d1-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a1d1-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a1d1-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="2a1d1-135">Asigna un valor de estado de NT a un valor <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a1d1-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2a1d1-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a1d1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a1d1-137">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="2a1d1-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

