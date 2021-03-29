---
description: Crea una interfaz ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'ISCardManage:: CreateCardAuth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652762"
---
# <a name="iscardmanagecreatecardauth-method"></a><span data-ttu-id="b018d-103">ISCardManage:: CreateCardAuth (método)</span><span class="sxs-lookup"><span data-stu-id="b018d-103">ISCardManage::CreateCardAuth method</span></span>

<span data-ttu-id="b018d-104">\[El método **CreateCardAuth** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b018d-104">\[The **CreateCardAuth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b018d-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b018d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b018d-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b018d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b018d-107">El método **CreateCardAuth** crea una interfaz [**ISCardAuth**](iscardauth.md) .</span><span class="sxs-lookup"><span data-stu-id="b018d-107">The **CreateCardAuth** method creates an [**ISCardAuth**](iscardauth.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b018d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b018d-108">Syntax</span></span>


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a><span data-ttu-id="b018d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b018d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b018d-110">*ppISCardAuth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b018d-110">*ppISCardAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b018d-111">Se devolvió un puntero a la interfaz creada.</span><span class="sxs-lookup"><span data-stu-id="b018d-111">Returned pointer to the created interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b018d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b018d-112">Return value</span></span>

<span data-ttu-id="b018d-113">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="b018d-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b018d-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b018d-114">Return code</span></span>                                                                                   | <span data-ttu-id="b018d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b018d-115">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="b018d-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b018d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b018d-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b018d-117">Operation completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="b018d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b018d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b018d-119">El parámetro *ppISCardAuth* no es válido.</span><span class="sxs-lookup"><span data-stu-id="b018d-119">The *ppISCardAuth* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b018d-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b018d-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b018d-121">Se pasó un puntero no válido en *ppISCardAuth*.</span><span class="sxs-lookup"><span data-stu-id="b018d-121">A bad pointer was passed in *ppISCardAuth*.</span></span><br/> |
| <dl> <span data-ttu-id="b018d-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b018d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b018d-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="b018d-123">Out of memory.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="b018d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b018d-124">Remarks</span></span>

<span data-ttu-id="b018d-125">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="b018d-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="b018d-126">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b018d-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b018d-127">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b018d-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b018d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b018d-128">Requirements</span></span>



| <span data-ttu-id="b018d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b018d-129">Requirement</span></span> | <span data-ttu-id="b018d-130">Value</span><span class="sxs-lookup"><span data-stu-id="b018d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b018d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b018d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b018d-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b018d-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b018d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b018d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b018d-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b018d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b018d-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b018d-135">End of client support</span></span><br/>    | <span data-ttu-id="b018d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b018d-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b018d-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b018d-137">End of server support</span></span><br/>    | <span data-ttu-id="b018d-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b018d-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b018d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b018d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b018d-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="b018d-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
