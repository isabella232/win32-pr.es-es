---
title: Método INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Recupera el número total de atributos del SoH.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Método GetNumberOfAttributes NAP
- Método GetNumberOfAttributes NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534156"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="42821-106">INapSoHProcessor:: GetNumberOfAttributes (método)</span><span class="sxs-lookup"><span data-stu-id="42821-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="42821-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="42821-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="42821-108">El método **INapSoHProcessor:: GetNumberOfAttributes** recupera el número total de atributos en el SOH.</span><span class="sxs-lookup"><span data-stu-id="42821-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="42821-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42821-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="42821-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42821-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42821-111">*attributeCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="42821-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42821-112">Puntero al número de atributos devueltos.</span><span class="sxs-lookup"><span data-stu-id="42821-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42821-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42821-113">Return value</span></span>

<span data-ttu-id="42821-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="42821-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="42821-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="42821-115">Return code</span></span>                                                                                     | <span data-ttu-id="42821-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="42821-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="42821-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="42821-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="42821-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="42821-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="42821-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="42821-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="42821-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="42821-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="42821-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="42821-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="42821-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="42821-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42821-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42821-123">Requirements</span></span>



| <span data-ttu-id="42821-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42821-124">Requirement</span></span> | <span data-ttu-id="42821-125">Value</span><span class="sxs-lookup"><span data-stu-id="42821-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="42821-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42821-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42821-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42821-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="42821-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42821-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42821-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42821-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="42821-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42821-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="42821-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="42821-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="42821-132">IDL</span><span class="sxs-lookup"><span data-stu-id="42821-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42821-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42821-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="42821-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42821-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42821-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42821-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="42821-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="42821-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42821-137">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="42821-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





