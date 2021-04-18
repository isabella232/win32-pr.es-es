---
description: La propiedad Property del objeto SummaryInfo establece u obtiene el valor de la propiedad especificada en la secuencia de información de resumen.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo. Property (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679453"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="847b4-103">SummaryInfo. Property (propiedad)</span><span class="sxs-lookup"><span data-stu-id="847b4-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="847b4-104">La propiedad **Property** del objeto [**SummaryInfo**](summaryinfo-object.md) establece u obtiene el valor de la propiedad especificada en la secuencia de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="847b4-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="847b4-105">Las propiedades se leen cuando se crea el objeto [**SummaryInfo**](summaryinfo-object.md) , pero no se escriben hasta que se llama al método [**Persist**](summaryinfo-persist.md) .</span><span class="sxs-lookup"><span data-stu-id="847b4-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="847b4-106">Establecer una propiedad en Empty provoca su eliminación; del mismo modo, si se solicita una propiedad inexistente, se devuelve un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="847b4-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="847b4-107">De lo contrario, los valores se pueden transferir como cadenas, enteros o tipos de fecha (fecha y hora).</span><span class="sxs-lookup"><span data-stu-id="847b4-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="847b4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="847b4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="847b4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="847b4-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="847b4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="847b4-110">Property value</span></span>

<span data-ttu-id="847b4-111">IDENTIFICADOR de propiedad obligatorio de una de las propiedades de resumen.</span><span class="sxs-lookup"><span data-stu-id="847b4-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="847b4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="847b4-112">Remarks</span></span>

<span data-ttu-id="847b4-113">**Identificadores de propiedad de Resumen estándar**</span><span class="sxs-lookup"><span data-stu-id="847b4-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="847b4-114">(no una enumeración)</span><span class="sxs-lookup"><span data-stu-id="847b4-114">(not an enumeration)</span></span>



| <span data-ttu-id="847b4-115">Nombre de parámetro</span><span class="sxs-lookup"><span data-stu-id="847b4-115">Parameter name</span></span>     | <span data-ttu-id="847b4-116">Value</span><span class="sxs-lookup"><span data-stu-id="847b4-116">Value</span></span> | <span data-ttu-id="847b4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="847b4-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="847b4-118">Diccionario de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="847b4-119">0</span><span class="sxs-lookup"><span data-stu-id="847b4-119">0</span></span>     | <span data-ttu-id="847b4-120">Formato especial, no compatible con el objeto SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="847b4-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="847b4-121">Página de códigos de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="847b4-122">1</span><span class="sxs-lookup"><span data-stu-id="847b4-122">1</span></span>     | <span data-ttu-id="847b4-123">I2 de VT \_</span><span class="sxs-lookup"><span data-stu-id="847b4-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="847b4-124">Título del PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-124">PID\_TITLE</span></span>         | <span data-ttu-id="847b4-125">2</span><span class="sxs-lookup"><span data-stu-id="847b4-125">2</span></span>     | <span data-ttu-id="847b4-126">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-127">asunto del PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="847b4-128">3</span><span class="sxs-lookup"><span data-stu-id="847b4-128">3</span></span>     | <span data-ttu-id="847b4-129">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-130">autor del PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="847b4-131">4</span><span class="sxs-lookup"><span data-stu-id="847b4-131">4</span></span>     | <span data-ttu-id="847b4-132">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-133">\_palabras clave de PID</span><span class="sxs-lookup"><span data-stu-id="847b4-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="847b4-134">5</span><span class="sxs-lookup"><span data-stu-id="847b4-134">5</span></span>     | <span data-ttu-id="847b4-135">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-136">Comentarios de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="847b4-137">6</span><span class="sxs-lookup"><span data-stu-id="847b4-137">6</span></span>     | <span data-ttu-id="847b4-138">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-139">plantilla de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="847b4-140">7</span><span class="sxs-lookup"><span data-stu-id="847b4-140">7</span></span>     | <span data-ttu-id="847b4-141">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-142">PID \_ LASTAUTHOR</span><span class="sxs-lookup"><span data-stu-id="847b4-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="847b4-143">8</span><span class="sxs-lookup"><span data-stu-id="847b4-143">8</span></span>     | <span data-ttu-id="847b4-144">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-145">PID \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="847b4-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="847b4-146">9</span><span class="sxs-lookup"><span data-stu-id="847b4-146">9</span></span>     | <span data-ttu-id="847b4-147">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-148">PID \_ EDITTIME</span><span class="sxs-lookup"><span data-stu-id="847b4-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="847b4-149">10</span><span class="sxs-lookup"><span data-stu-id="847b4-149">10</span></span>    | <span data-ttu-id="847b4-150">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="847b4-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="847b4-151">PID \_ LASTPRINTED</span><span class="sxs-lookup"><span data-stu-id="847b4-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="847b4-152">11</span><span class="sxs-lookup"><span data-stu-id="847b4-152">11</span></span>    | <span data-ttu-id="847b4-153">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="847b4-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="847b4-154">PID \_ Create \_ DTM</span><span class="sxs-lookup"><span data-stu-id="847b4-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="847b4-155">12</span><span class="sxs-lookup"><span data-stu-id="847b4-155">12</span></span>    | <span data-ttu-id="847b4-156">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="847b4-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="847b4-157">PID \_ LASTSAVE \_ DTM</span><span class="sxs-lookup"><span data-stu-id="847b4-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="847b4-158">13</span><span class="sxs-lookup"><span data-stu-id="847b4-158">13</span></span>    | <span data-ttu-id="847b4-159">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="847b4-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="847b4-160">PID \_ PAGECOUNT</span><span class="sxs-lookup"><span data-stu-id="847b4-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="847b4-161">14</span><span class="sxs-lookup"><span data-stu-id="847b4-161">14</span></span>    | <span data-ttu-id="847b4-162">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="847b4-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="847b4-163">PID \_ WORDCOUNT</span><span class="sxs-lookup"><span data-stu-id="847b4-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="847b4-164">15</span><span class="sxs-lookup"><span data-stu-id="847b4-164">15</span></span>    | <span data-ttu-id="847b4-165">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="847b4-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="847b4-166">CHARCOUNT de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="847b4-167">16</span><span class="sxs-lookup"><span data-stu-id="847b4-167">16</span></span>    | <span data-ttu-id="847b4-168">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="847b4-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="847b4-169">miniatura de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="847b4-170">17</span><span class="sxs-lookup"><span data-stu-id="847b4-170">17</span></span>    | <span data-ttu-id="847b4-171">VT \_ CF (no compatible)</span><span class="sxs-lookup"><span data-stu-id="847b4-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="847b4-172">PID \_ APPNAME</span><span class="sxs-lookup"><span data-stu-id="847b4-172">PID\_APPNAME</span></span>       | <span data-ttu-id="847b4-173">18</span><span class="sxs-lookup"><span data-stu-id="847b4-173">18</span></span>    | <span data-ttu-id="847b4-174">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="847b4-175">seguridad de PID \_</span><span class="sxs-lookup"><span data-stu-id="847b4-175">PID\_SECURITY</span></span>      | <span data-ttu-id="847b4-176">19</span><span class="sxs-lookup"><span data-stu-id="847b4-176">19</span></span>    | <span data-ttu-id="847b4-177">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="847b4-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="847b4-178">**Tipos de datos de las propiedades**</span><span class="sxs-lookup"><span data-stu-id="847b4-178">**Property Data Types**</span></span>

<span data-ttu-id="847b4-179">(no una enumeración)</span><span class="sxs-lookup"><span data-stu-id="847b4-179">(not an enumeration)</span></span>



| <span data-ttu-id="847b4-180">Nombre de parámetro</span><span class="sxs-lookup"><span data-stu-id="847b4-180">Parameter name</span></span> | <span data-ttu-id="847b4-181">Value</span><span class="sxs-lookup"><span data-stu-id="847b4-181">Value</span></span> | <span data-ttu-id="847b4-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="847b4-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="847b4-183">I2 de VT \_</span><span class="sxs-lookup"><span data-stu-id="847b4-183">VT\_I2</span></span>         | <span data-ttu-id="847b4-184">2</span><span class="sxs-lookup"><span data-stu-id="847b4-184">2</span></span>     | <span data-ttu-id="847b4-185">Entero de 16 bits</span><span class="sxs-lookup"><span data-stu-id="847b4-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="847b4-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="847b4-186">VT\_I4</span></span>         | <span data-ttu-id="847b4-187">3</span><span class="sxs-lookup"><span data-stu-id="847b4-187">3</span></span>     | <span data-ttu-id="847b4-188">Entero de 32 bits</span><span class="sxs-lookup"><span data-stu-id="847b4-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="847b4-189">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="847b4-189">VT\_LPSTR</span></span>      | <span data-ttu-id="847b4-190">30</span><span class="sxs-lookup"><span data-stu-id="847b4-190">30</span></span>    | <span data-ttu-id="847b4-191">String</span><span class="sxs-lookup"><span data-stu-id="847b4-191">String</span></span>                                                                                   |
| <span data-ttu-id="847b4-192">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="847b4-192">VT\_FILETIME</span></span>   | <span data-ttu-id="847b4-193">64</span><span class="sxs-lookup"><span data-stu-id="847b4-193">64</span></span>    | <span data-ttu-id="847b4-194">Fecha y hora (FILETIME, convertido a la hora de variante)</span><span class="sxs-lookup"><span data-stu-id="847b4-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="847b4-195">VT \_ CF</span><span class="sxs-lookup"><span data-stu-id="847b4-195">VT\_CF</span></span>         | <span data-ttu-id="847b4-196">71</span><span class="sxs-lookup"><span data-stu-id="847b4-196">71</span></span>    | <span data-ttu-id="847b4-197">Formato del portapapeles + datos, no administrados por el objeto [**SummaryInfo**](summaryinfo-object.md)</span><span class="sxs-lookup"><span data-stu-id="847b4-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="847b4-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="847b4-198">Requirements</span></span>



| <span data-ttu-id="847b4-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="847b4-199">Requirement</span></span> | <span data-ttu-id="847b4-200">Value</span><span class="sxs-lookup"><span data-stu-id="847b4-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="847b4-201">Versión</span><span class="sxs-lookup"><span data-stu-id="847b4-201">Version</span></span><br/> | <span data-ttu-id="847b4-202">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="847b4-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="847b4-203">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="847b4-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="847b4-204">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="847b4-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="847b4-205">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="847b4-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="847b4-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="847b4-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="847b4-207">IID</span><span class="sxs-lookup"><span data-stu-id="847b4-207">IID</span></span><br/>     | <span data-ttu-id="847b4-208">IID \_ ISummaryInfo se define como 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="847b4-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="847b4-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="847b4-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847b4-210">**MsiSummaryInfoSetProperty**</span><span class="sxs-lookup"><span data-stu-id="847b4-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="847b4-211">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="847b4-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




