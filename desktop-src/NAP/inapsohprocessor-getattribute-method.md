---
title: Método GetAttribute INapSoHProcessor (NapProtocol. h)
description: Recupera el tipo y el valor del atributo, según la ubicación del atributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute (método) NAP
- Método GetAttribute NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método GetAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676581"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="6883d-106">INapSoHProcessor:: GetAttribute (método)</span><span class="sxs-lookup"><span data-stu-id="6883d-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="6883d-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6883d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6883d-108">El método **INapSoHProcessor:: getAttribute** recupera el tipo de atributo y el valor, según la ubicación del atributo.</span><span class="sxs-lookup"><span data-stu-id="6883d-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="6883d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6883d-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="6883d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6883d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6883d-111">*attributeLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6883d-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6883d-112">La ubicación (índice) del atributo cuyo tipo y valor se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6883d-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="6883d-113">El valor de *attributeLocation* se devuelve de una llamada anterior a [**INapSoHProcessor:: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span><span class="sxs-lookup"><span data-stu-id="6883d-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="6883d-114">*tipo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6883d-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6883d-115">Puntero a una estructura [**SoHAttributeType**](sohattributetype-enum.md) que especifica el tipo del atributo en el *valor*.</span><span class="sxs-lookup"><span data-stu-id="6883d-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="6883d-116">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6883d-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6883d-117">Un puntero a un puntero a una estructura [**SoHAttributeValue**](sohattributevalue-union.md) que contiene el valor del atributo tal y como lo define el *tipo*.</span><span class="sxs-lookup"><span data-stu-id="6883d-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6883d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6883d-118">Return value</span></span>

<span data-ttu-id="6883d-119">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="6883d-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6883d-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6883d-120">Return code</span></span>                                                                                     | <span data-ttu-id="6883d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6883d-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6883d-122"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="6883d-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6883d-123">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6883d-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6883d-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6883d-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6883d-125">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="6883d-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6883d-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6883d-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6883d-127">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="6883d-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6883d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6883d-128">Requirements</span></span>



| <span data-ttu-id="6883d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6883d-129">Requirement</span></span> | <span data-ttu-id="6883d-130">Value</span><span class="sxs-lookup"><span data-stu-id="6883d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6883d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6883d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6883d-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6883d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6883d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6883d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6883d-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6883d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6883d-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6883d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6883d-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="6883d-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="6883d-137">IDL</span><span class="sxs-lookup"><span data-stu-id="6883d-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6883d-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6883d-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="6883d-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6883d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6883d-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6883d-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6883d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="6883d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6883d-142">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="6883d-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





