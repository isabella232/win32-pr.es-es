---
description: Crea la interfaz especificada.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'ISCardManage:: CreateInterface (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278136"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="639af-103">ISCardManage:: CreateInterface (método)</span><span class="sxs-lookup"><span data-stu-id="639af-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="639af-104">\[El método **CreateInterface** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="639af-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="639af-105">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="639af-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="639af-106">El método **CreateInterface** crea la interfaz especificada.</span><span class="sxs-lookup"><span data-stu-id="639af-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="639af-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="639af-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="639af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="639af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639af-109">*pguidInterface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="639af-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="639af-110">Valor GUID de la interfaz que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="639af-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="639af-111">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="639af-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="639af-112">Nombre de la interfaz que se va a crear si el GUID no está disponible.</span><span class="sxs-lookup"><span data-stu-id="639af-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="639af-113">Los valores estándar son "CryptoProvider".</span><span class="sxs-lookup"><span data-stu-id="639af-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="639af-114">*pUserData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="639af-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="639af-115">Puntero a los datos específicos del usuario que se van a usar en la creación de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="639af-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="639af-116">*ppInterface* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="639af-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="639af-117">Puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="639af-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="639af-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="639af-118">Return value</span></span>

<span data-ttu-id="639af-119">Los posibles valores devueltos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="639af-119">The possible return values are the following:</span></span>



| <span data-ttu-id="639af-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="639af-120">Return code</span></span>                                                                                   | <span data-ttu-id="639af-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="639af-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="639af-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="639af-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="639af-123">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="639af-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="639af-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="639af-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="639af-125">Uno de los parámetros proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="639af-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="639af-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="639af-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="639af-127">Se pasó un puntero incorrecto en el parámetro *pguidInterface* o *pUserData* .</span><span class="sxs-lookup"><span data-stu-id="639af-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="639af-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="639af-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="639af-129">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="639af-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="639af-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="639af-130">Remarks</span></span>

<span data-ttu-id="639af-131">Para obtener una lista de todos los métodos definidos por la interfaz [**ISCardManage**](iscardmanage.md) , vea **ISCardManage**.</span><span class="sxs-lookup"><span data-stu-id="639af-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="639af-132">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="639af-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="639af-133">Para obtener información sobre los códigos de error de las tarjetas inteligentes, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="639af-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="639af-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="639af-134">Requirements</span></span>



| <span data-ttu-id="639af-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="639af-135">Requirement</span></span> | <span data-ttu-id="639af-136">Value</span><span class="sxs-lookup"><span data-stu-id="639af-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="639af-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="639af-137">Minimum supported client</span></span><br/> | <span data-ttu-id="639af-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="639af-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="639af-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="639af-139">Minimum supported server</span></span><br/> | <span data-ttu-id="639af-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="639af-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="639af-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="639af-141">End of client support</span></span><br/>    | <span data-ttu-id="639af-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="639af-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="639af-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="639af-143">End of server support</span></span><br/>    | <span data-ttu-id="639af-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="639af-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="639af-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="639af-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639af-146">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="639af-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
