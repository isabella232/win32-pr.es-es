---
description: Usa llamadas secuenciales para recuperar todas las cadenas dentro de los intervalos especificados.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Función GetStringsFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000921"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="ed763-103">GetStringsFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="ed763-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="ed763-104">La función **GetStringsFromBlob** usa llamadas secuenciales para recuperar todas las cadenas dentro de los intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="ed763-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed763-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed763-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="ed763-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed763-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed763-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ed763-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-109">*pRequestedOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed763-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-110">Un puntero a la sección del propietario de la que se va a obtener la cadena.</span><span class="sxs-lookup"><span data-stu-id="ed763-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-111">*pRequestedCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed763-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-112">Un puntero a la sección de categoría de la que se va a obtener la cadena.</span><span class="sxs-lookup"><span data-stu-id="ed763-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-113">*pRequestedTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed763-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-114">Puntero a la etiqueta para la cadena solicitada.</span><span class="sxs-lookup"><span data-stu-id="ed763-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-115">*ppReturnedOwnerName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed763-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-116">Puntero a la variable que apunta a donde se devolverá el nombre del **propietario** .</span><span class="sxs-lookup"><span data-stu-id="ed763-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-117">*ppReturnedCategoryName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed763-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-118">Puntero a la variable que apunta a donde se devolverá el nombre de la **categoría** .</span><span class="sxs-lookup"><span data-stu-id="ed763-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-119">*ppReturnedTagName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed763-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-120">Puntero a la variable que apunta a donde se devolverá el nombre de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="ed763-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-121">*ppReturnedString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed763-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-122">Puntero a la variable que apunta a donde se devolverá el nombre de la cadena.</span><span class="sxs-lookup"><span data-stu-id="ed763-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ed763-123">*pRestartKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed763-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed763-124">Puntero a la variable donde se especificará y devolverá la clave de reinicio.</span><span class="sxs-lookup"><span data-stu-id="ed763-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed763-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed763-125">Return value</span></span>

<span data-ttu-id="ed763-126">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ed763-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ed763-127">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el problema.</span><span class="sxs-lookup"><span data-stu-id="ed763-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="ed763-128">Si no existe una combinación especificada de información de **propietario**, **categoría** y **etiqueta** , el valor devuelto es **NMERR la entrada de \_ BLOB no \_ \_ \_ \_ existe**.</span><span class="sxs-lookup"><span data-stu-id="ed763-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="ed763-129">Cuando el BLOB se atraviesa completamente dentro de los límites especificados inicialmente, la función devuelve **la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe** y el parámetro *pRestartKey* apunta a cero.</span><span class="sxs-lookup"><span data-stu-id="ed763-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed763-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed763-130">Remarks</span></span>

<span data-ttu-id="ed763-131">En la llamada inicial a la función **GetStringsFromBlob** , el parámetro *pRestartKey* apunta a una variable que contiene el valor cero.</span><span class="sxs-lookup"><span data-stu-id="ed763-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="ed763-132">Los parámetros *prequested* solo se pueden usar cuando la clave restart es cero.</span><span class="sxs-lookup"><span data-stu-id="ed763-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="ed763-133">En las llamadas posteriores, cuando *pRestartKey* tiene valores distintos de cero, se omiten los parámetros *prequested* .</span><span class="sxs-lookup"><span data-stu-id="ed763-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="ed763-134">En la llamada inicial, All puede señalar a **null**, que configura la consulta para que devuelva todas las entradas del BLOB, una por cada llamada subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="ed763-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="ed763-135">Al especificar un propietario, se limitan las cadenas devueltas solo a ese propietario.</span><span class="sxs-lookup"><span data-stu-id="ed763-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="ed763-136">Se aplica una limitación similar para las categorías y las etiquetas, con la ADVERTENCIA adicional de que, si se especifica una categoría, también se debe especificar un propietario y, si se especifica una etiqueta, se debe especificar una categoría (y, por tanto, un propietario).</span><span class="sxs-lookup"><span data-stu-id="ed763-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="ed763-137">Cuando se devuelve la llamada inicial a **GetStringsFromBlob** , *pRestartKey* apunta a un nuevo valor, que se debe especificar en la siguiente llamada a la función para obtener el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="ed763-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed763-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed763-138">Requirements</span></span>



| <span data-ttu-id="ed763-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed763-139">Requirement</span></span> | <span data-ttu-id="ed763-140">Value</span><span class="sxs-lookup"><span data-stu-id="ed763-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed763-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed763-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ed763-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ed763-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ed763-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed763-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ed763-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed763-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed763-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed763-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed763-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed763-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ed763-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed763-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed763-148"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed763-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ed763-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed763-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed763-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed763-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed763-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed763-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed763-152">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-153">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-154">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-155">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-156">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-157">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-158">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-159">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-160">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="ed763-161">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="ed763-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 




