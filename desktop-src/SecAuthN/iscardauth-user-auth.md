---
description: El método de autenticación de usuario \_ permite el acceso a los servicios de autenticación de usuario.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'ISCardAuth:: User_Auth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907869"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="7e7b7-103">ISCardAuth:: User \_ auth (método)</span><span class="sxs-lookup"><span data-stu-id="7e7b7-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="7e7b7-104">\[El método de **\_ autenticación de usuario** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7e7b7-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e7b7-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7e7b7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7e7b7-107">El método de autenticación de **usuario \_** permite el acceso a los servicios de autenticación de usuario.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7b7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e7b7-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7e7b7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e7b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e7b7-110">*lAlgorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e7b7-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e7b7-111">Algoritmo que se va a usar en el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="7e7b7-112">*pParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e7b7-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e7b7-113">Un objeto [**IByteBuffer**](ibytebuffer.md) que contiene los parámetros específicos del proveedor del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="7e7b7-114">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e7b7-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e7b7-115">Datos que se van a usar en el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e7b7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e7b7-116">Return value</span></span>

<span data-ttu-id="7e7b7-117">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7e7b7-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7e7b7-118">Return code</span></span>                                                                                   | <span data-ttu-id="7e7b7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e7b7-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7e7b7-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7e7b7-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7e7b7-121">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7e7b7-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7e7b7-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7e7b7-123">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="7e7b7-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e7b7-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7e7b7-125">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="7e7b7-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7e7b7-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7e7b7-127">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="7e7b7-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7e7b7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7b7-128">Remarks</span></span>

<span data-ttu-id="7e7b7-129">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="7e7b7-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="7e7b7-130">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e7b7-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7e7b7-131">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7e7b7-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7b7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7b7-132">Requirements</span></span>



| <span data-ttu-id="7e7b7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7b7-133">Requirement</span></span> | <span data-ttu-id="7e7b7-134">Value</span><span class="sxs-lookup"><span data-stu-id="7e7b7-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e7b7-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e7b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7b7-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7e7b7-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7e7b7-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e7b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7b7-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e7b7-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7e7b7-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7e7b7-139">End of client support</span></span><br/>    | <span data-ttu-id="7e7b7-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e7b7-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="7e7b7-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7e7b7-141">End of server support</span></span><br/>    | <span data-ttu-id="7e7b7-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e7b7-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="7e7b7-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e7b7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7b7-144">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="7e7b7-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="7e7b7-145">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="7e7b7-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
