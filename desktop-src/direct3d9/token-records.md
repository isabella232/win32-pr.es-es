---
description: En esta sección se describe el formato de los registros de cada uno de los tokens del cojinete de registros. La información se divide en las secciones siguientes.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Registros de token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714775"
---
# <a name="token-records"></a><span data-ttu-id="5f2d2-104">Registros de token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-104">Token Records</span></span>

<span data-ttu-id="5f2d2-105">En esta sección se describe el formato de los registros de cada uno de los tokens del cojinete de registros.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="5f2d2-106">La información se divide en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="5f2d2-107">nombre del TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="5f2d2-108">cadena de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="5f2d2-109">entero de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="5f2d2-110">GUID de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="5f2d2-111">lista de enteros de TOKEN \_ \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="5f2d2-112">\_lista de Float de token \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="5f2d2-113">nombre del TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-113">TOKEN\_NAME</span></span>

<span data-ttu-id="5f2d2-114">Un registro de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-114">A variable-length record.</span></span> <span data-ttu-id="5f2d2-115">El token va seguido de un valor de recuento que especifica el número de bytes que siguen en el campo de nombre.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="5f2d2-116">Un nombre ASCII de recuento de longitud completa el registro.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="5f2d2-117">Campo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-117">Field</span></span> | <span data-ttu-id="5f2d2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-118">Type</span></span>       | <span data-ttu-id="5f2d2-119">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="5f2d2-119">Size (bytes)</span></span> | <span data-ttu-id="5f2d2-120">Contenido</span><span class="sxs-lookup"><span data-stu-id="5f2d2-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="5f2d2-121">token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-121">token</span></span> | <span data-ttu-id="5f2d2-122">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-122">WORD</span></span>       | <span data-ttu-id="5f2d2-123">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-123">2</span></span>            | <span data-ttu-id="5f2d2-124">nombre del token \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-124">token\_name</span></span>                    |
| <span data-ttu-id="5f2d2-125">count</span><span class="sxs-lookup"><span data-stu-id="5f2d2-125">count</span></span> | <span data-ttu-id="5f2d2-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-126">DWORD</span></span>      | <span data-ttu-id="5f2d2-127">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-127">4</span></span>            | <span data-ttu-id="5f2d2-128">Longitud del campo de nombre, en bytes</span><span class="sxs-lookup"><span data-stu-id="5f2d2-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="5f2d2-129">name</span><span class="sxs-lookup"><span data-stu-id="5f2d2-129">name</span></span>  | <span data-ttu-id="5f2d2-130">Matriz de BYTEs</span><span class="sxs-lookup"><span data-stu-id="5f2d2-130">BYTE array</span></span> | <span data-ttu-id="5f2d2-131">count</span><span class="sxs-lookup"><span data-stu-id="5f2d2-131">count</span></span>        | <span data-ttu-id="5f2d2-132">Nombre ASCII</span><span class="sxs-lookup"><span data-stu-id="5f2d2-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="5f2d2-133">cadena de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-133">TOKEN\_STRING</span></span>

<span data-ttu-id="5f2d2-134">Un registro de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-134">A variable-length record.</span></span> <span data-ttu-id="5f2d2-135">El token va seguido de un valor de recuento que especifica el número de bytes que siguen en el campo de cadena.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="5f2d2-136">Una cadena ASCII de recuento de longitud continúa el registro, que se completa mediante un token de terminación.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="5f2d2-137">La elección del terminador viene determinada por los problemas de sintaxis descritos en otros lugares.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="5f2d2-138">Campo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-138">Field</span></span>      | <span data-ttu-id="5f2d2-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-139">Type</span></span>       | <span data-ttu-id="5f2d2-140">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="5f2d2-140">Size (bytes)</span></span> | <span data-ttu-id="5f2d2-141">Contenido</span><span class="sxs-lookup"><span data-stu-id="5f2d2-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="5f2d2-142">token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-142">token</span></span>      | <span data-ttu-id="5f2d2-143">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-143">WORD</span></span>       | <span data-ttu-id="5f2d2-144">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-144">2</span></span>            | <span data-ttu-id="5f2d2-145">cadena de token \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-145">token\_string</span></span>                    |
| <span data-ttu-id="5f2d2-146">count</span><span class="sxs-lookup"><span data-stu-id="5f2d2-146">count</span></span>      | <span data-ttu-id="5f2d2-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-147">DWORD</span></span>      | <span data-ttu-id="5f2d2-148">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-148">4</span></span>            | <span data-ttu-id="5f2d2-149">Longitud del campo de cadena en bytes</span><span class="sxs-lookup"><span data-stu-id="5f2d2-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="5f2d2-150">String@</span><span class="sxs-lookup"><span data-stu-id="5f2d2-150">strinG</span></span>     | <span data-ttu-id="5f2d2-151">Matriz de BYTEs</span><span class="sxs-lookup"><span data-stu-id="5f2d2-151">BYTE array</span></span> | <span data-ttu-id="5f2d2-152">count</span><span class="sxs-lookup"><span data-stu-id="5f2d2-152">count</span></span>        | <span data-ttu-id="5f2d2-153">Cadena ASCII</span><span class="sxs-lookup"><span data-stu-id="5f2d2-153">ASCII string</span></span>                     |
| <span data-ttu-id="5f2d2-154">terminado</span><span class="sxs-lookup"><span data-stu-id="5f2d2-154">terminator</span></span> | <span data-ttu-id="5f2d2-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-155">DWORD</span></span>      | <span data-ttu-id="5f2d2-156">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-156">4</span></span>            | <span data-ttu-id="5f2d2-157">\_punto y \_ coma del token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="5f2d2-158">entero de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="5f2d2-159">Un registro de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-159">A fixed length record.</span></span> <span data-ttu-id="5f2d2-160">El token va seguido del valor entero requerido.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="5f2d2-161">Campo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-161">Field</span></span> | <span data-ttu-id="5f2d2-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-162">Type</span></span>  | <span data-ttu-id="5f2d2-163">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="5f2d2-163">Size (bytes)</span></span> | <span data-ttu-id="5f2d2-164">Contenido</span><span class="sxs-lookup"><span data-stu-id="5f2d2-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="5f2d2-165">token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-165">token</span></span> | <span data-ttu-id="5f2d2-166">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-166">WORD</span></span>  | <span data-ttu-id="5f2d2-167">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-167">2</span></span>            | <span data-ttu-id="5f2d2-168">entero de tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="5f2d2-169">Valor</span><span class="sxs-lookup"><span data-stu-id="5f2d2-169">valuE</span></span> | <span data-ttu-id="5f2d2-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-170">DWORD</span></span> | <span data-ttu-id="5f2d2-171">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-171">4</span></span>            | <span data-ttu-id="5f2d2-172">Entero único</span><span class="sxs-lookup"><span data-stu-id="5f2d2-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="5f2d2-173">GUID de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-173">TOKEN\_GUID</span></span>

<span data-ttu-id="5f2d2-174">Un registro de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-174">A fixed-length record.</span></span> <span data-ttu-id="5f2d2-175">El token va seguido de los cuatro campos de datos tal y como se define en el estándar de OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="5f2d2-176">Campo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-176">Field</span></span> | <span data-ttu-id="5f2d2-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-177">Type</span></span>       | <span data-ttu-id="5f2d2-178">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="5f2d2-178">Size (bytes)</span></span> | <span data-ttu-id="5f2d2-179">Contenido</span><span class="sxs-lookup"><span data-stu-id="5f2d2-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="5f2d2-180">token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-180">token</span></span> | <span data-ttu-id="5f2d2-181">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-181">WORD</span></span>       | <span data-ttu-id="5f2d2-182">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-182">2</span></span>            | <span data-ttu-id="5f2d2-183">GUID de tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="5f2d2-184">Data1</span><span class="sxs-lookup"><span data-stu-id="5f2d2-184">Data1</span></span> | <span data-ttu-id="5f2d2-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-185">DWORD</span></span>      | <span data-ttu-id="5f2d2-186">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-186">4</span></span>            | <span data-ttu-id="5f2d2-187">Campo de datos UUID 1</span><span class="sxs-lookup"><span data-stu-id="5f2d2-187">UUID data field 1</span></span> |
| <span data-ttu-id="5f2d2-188">Data2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-188">Data2</span></span> | <span data-ttu-id="5f2d2-189">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-189">WORD</span></span>       | <span data-ttu-id="5f2d2-190">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-190">2</span></span>            | <span data-ttu-id="5f2d2-191">Campo de datos UUID 2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-191">UUID data field 2</span></span> |
| <span data-ttu-id="5f2d2-192">Data3</span><span class="sxs-lookup"><span data-stu-id="5f2d2-192">Data3</span></span> | <span data-ttu-id="5f2d2-193">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-193">WORD</span></span>       | <span data-ttu-id="5f2d2-194">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-194">2</span></span>            | <span data-ttu-id="5f2d2-195">Campo de datos UUID 3</span><span class="sxs-lookup"><span data-stu-id="5f2d2-195">UUID data field 3</span></span> |
| <span data-ttu-id="5f2d2-196">Data4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-196">Data4</span></span> | <span data-ttu-id="5f2d2-197">Matriz de BYTEs</span><span class="sxs-lookup"><span data-stu-id="5f2d2-197">BYTE array</span></span> | <span data-ttu-id="5f2d2-198">8</span><span class="sxs-lookup"><span data-stu-id="5f2d2-198">8</span></span>            | <span data-ttu-id="5f2d2-199">Campo de datos UUID 4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="5f2d2-200">lista de enteros de TOKEN \_ \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="5f2d2-201">Un registro de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-201">A variable-length record.</span></span> <span data-ttu-id="5f2d2-202">El token va seguido de un valor de recuento que especifica el número de enteros que siguen en el campo de lista.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="5f2d2-203">Por motivos de eficacia, las listas de enteros consecutivas se deben crear en una sola lista.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="5f2d2-204">Campo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-204">Field</span></span> | <span data-ttu-id="5f2d2-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-205">Type</span></span>  | <span data-ttu-id="5f2d2-206">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="5f2d2-206">Size (bytes)</span></span> | <span data-ttu-id="5f2d2-207">Contenido</span><span class="sxs-lookup"><span data-stu-id="5f2d2-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="5f2d2-208">token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-208">token</span></span> | <span data-ttu-id="5f2d2-209">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-209">WORD</span></span>  | <span data-ttu-id="5f2d2-210">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-210">2</span></span>            | <span data-ttu-id="5f2d2-211">lista de enteros de tOKEN \_ \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="5f2d2-212">count</span><span class="sxs-lookup"><span data-stu-id="5f2d2-212">count</span></span> | <span data-ttu-id="5f2d2-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-213">DWORD</span></span> | <span data-ttu-id="5f2d2-214">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-214">4</span></span>            | <span data-ttu-id="5f2d2-215">Número de enteros en el campo de lista</span><span class="sxs-lookup"><span data-stu-id="5f2d2-215">Number of integers in list field</span></span> |
| <span data-ttu-id="5f2d2-216">list</span><span class="sxs-lookup"><span data-stu-id="5f2d2-216">list</span></span>  | <span data-ttu-id="5f2d2-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-217">DWORD</span></span> | <span data-ttu-id="5f2d2-218">4 x recuento</span><span class="sxs-lookup"><span data-stu-id="5f2d2-218">4 x count</span></span>    | <span data-ttu-id="5f2d2-219">Lista de enteros</span><span class="sxs-lookup"><span data-stu-id="5f2d2-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="5f2d2-220">\_lista de Float de token \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="5f2d2-221">Un registro de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-221">A variable-length record.</span></span> <span data-ttu-id="5f2d2-222">El token va seguido de un valor de recuento que especifica el número de valores float o Double que siguen en el campo de lista.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="5f2d2-223">El valor de Float sizespecified en el encabezado de archivo determina el tamaño del valor de punto flotante (float o Double).</span><span class="sxs-lookup"><span data-stu-id="5f2d2-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="5f2d2-224">Por motivos de eficacia, las listas de punto flotante de TOKENs consecutivos \_ \_ deben crearse en una sola lista.</span><span class="sxs-lookup"><span data-stu-id="5f2d2-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="5f2d2-225">Campo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-225">Field</span></span> | <span data-ttu-id="5f2d2-226">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2d2-226">Type</span></span>               | <span data-ttu-id="5f2d2-227">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="5f2d2-227">Size (bytes)</span></span>   | <span data-ttu-id="5f2d2-228">Contenido</span><span class="sxs-lookup"><span data-stu-id="5f2d2-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="5f2d2-229">token</span><span class="sxs-lookup"><span data-stu-id="5f2d2-229">token</span></span> | <span data-ttu-id="5f2d2-230">WORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-230">WORD</span></span>               | <span data-ttu-id="5f2d2-231">2</span><span class="sxs-lookup"><span data-stu-id="5f2d2-231">2</span></span>              | <span data-ttu-id="5f2d2-232">\_lista de Float de tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="5f2d2-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="5f2d2-233">count</span><span class="sxs-lookup"><span data-stu-id="5f2d2-233">count</span></span> | <span data-ttu-id="5f2d2-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f2d2-234">DWORD</span></span>              | <span data-ttu-id="5f2d2-235">4</span><span class="sxs-lookup"><span data-stu-id="5f2d2-235">4</span></span>              | <span data-ttu-id="5f2d2-236">Número de valores float o Double en el campo de lista</span><span class="sxs-lookup"><span data-stu-id="5f2d2-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="5f2d2-237">list</span><span class="sxs-lookup"><span data-stu-id="5f2d2-237">list</span></span>  | <span data-ttu-id="5f2d2-238">matriz float/double</span><span class="sxs-lookup"><span data-stu-id="5f2d2-238">float/double array</span></span> | <span data-ttu-id="5f2d2-239">número 4 u 8 x</span><span class="sxs-lookup"><span data-stu-id="5f2d2-239">4 or 8 x count</span></span> | <span data-ttu-id="5f2d2-240">Lista de valores float o Double</span><span class="sxs-lookup"><span data-stu-id="5f2d2-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="5f2d2-241">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f2d2-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f2d2-242">Codificación binaria</span><span class="sxs-lookup"><span data-stu-id="5f2d2-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 
