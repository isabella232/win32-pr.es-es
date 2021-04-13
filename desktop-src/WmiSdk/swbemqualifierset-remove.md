---
description: El método Remove del objeto SWbemQualifierSet elimina un calificador con nombre de la colección.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544654"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="623c6-103">SWbemQualifierSet. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="623c6-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="623c6-104">El método **Remove** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) elimina un calificador con nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="623c6-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="623c6-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="623c6-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="623c6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="623c6-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="623c6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="623c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623c6-108">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="623c6-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623c6-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="623c6-109">Required.</span></span> <span data-ttu-id="623c6-110">Nombre del calificador que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="623c6-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="623c6-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="623c6-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="623c6-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="623c6-112">Reserved.</span></span> <span data-ttu-id="623c6-113">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="623c6-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623c6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="623c6-114">Return value</span></span>

<span data-ttu-id="623c6-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="623c6-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="623c6-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="623c6-116">Error codes</span></span>

<span data-ttu-id="623c6-117">Después de completar el método **Remove** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="623c6-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="623c6-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="623c6-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="623c6-119">El parámetro *iFlags* no era válido.</span><span class="sxs-lookup"><span data-stu-id="623c6-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="623c6-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="623c6-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="623c6-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="623c6-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="623c6-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="623c6-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="623c6-123">El calificador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="623c6-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="623c6-124">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="623c6-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="623c6-125">Quitar este calificador no es válido.</span><span class="sxs-lookup"><span data-stu-id="623c6-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="623c6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="623c6-126">Remarks</span></span>

<span data-ttu-id="623c6-127">No se puede recorrer en iteración una colección mientras se quitan elementos porque cuando se quita un elemento de una colección, el puntero de la colección se mueve al siguiente elemento.</span><span class="sxs-lookup"><span data-stu-id="623c6-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="623c6-128">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="623c6-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="623c6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623c6-129">Requirements</span></span>



| <span data-ttu-id="623c6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="623c6-130">Requirement</span></span> | <span data-ttu-id="623c6-131">Value</span><span class="sxs-lookup"><span data-stu-id="623c6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="623c6-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623c6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="623c6-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="623c6-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="623c6-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623c6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="623c6-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="623c6-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="623c6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="623c6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="623c6-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="623c6-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="623c6-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="623c6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="623c6-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="623c6-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="623c6-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="623c6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="623c6-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="623c6-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="623c6-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="623c6-142">CLSID</span></span><br/>                    | <span data-ttu-id="623c6-143">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="623c6-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="623c6-144">IID</span><span class="sxs-lookup"><span data-stu-id="623c6-144">IID</span></span><br/>                      | <span data-ttu-id="623c6-145">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="623c6-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="623c6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="623c6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623c6-147">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="623c6-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="623c6-148">**SWbemQualifierSet. Add**</span><span class="sxs-lookup"><span data-stu-id="623c6-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




