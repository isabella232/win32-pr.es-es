---
description: El método de autenticación de la aplicación \_ autentica la aplicación. Permite que una aplicación se autentique a sí misma (mediante un protocolo de desafío/firma) cuando una tarjeta inteligente solicita la autenticación.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'ISCardAuth:: APP_Auth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908432"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="37508-104">ISCardAuth:: APP \_ auth (método)</span><span class="sxs-lookup"><span data-stu-id="37508-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="37508-105">\[El método de **\_ autenticación** de la aplicación está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="37508-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="37508-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="37508-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="37508-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="37508-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="37508-108">El método de **\_ autenticación** de la aplicación autentica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37508-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="37508-109">Permite que una aplicación se autentique a sí misma (mediante un protocolo de desafío/firma) cuando una [*tarjeta inteligente*](../secgloss/s-gly.md)solicita la autenticación.</span><span class="sxs-lookup"><span data-stu-id="37508-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="37508-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37508-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="37508-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37508-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37508-112">*lAlgoID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37508-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37508-113">Algoritmo que se va a usar en el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="37508-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="37508-114">*pParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37508-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37508-115">[**IByteBuffer**](ibytebuffer.md) que contiene los parámetros específicos del proveedor del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="37508-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="37508-116">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37508-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37508-117">Datos necesarios para el cálculo.</span><span class="sxs-lookup"><span data-stu-id="37508-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37508-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37508-118">Return value</span></span>

<span data-ttu-id="37508-119">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="37508-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="37508-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="37508-120">Return code</span></span>                                                                                   | <span data-ttu-id="37508-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="37508-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="37508-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="37508-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="37508-123">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="37508-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="37508-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="37508-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="37508-125">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="37508-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="37508-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="37508-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="37508-127">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="37508-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="37508-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="37508-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="37508-129">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="37508-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="37508-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37508-130">Remarks</span></span>

<span data-ttu-id="37508-131">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="37508-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="37508-132">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37508-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="37508-133">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="37508-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37508-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37508-134">Requirements</span></span>



| <span data-ttu-id="37508-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="37508-135">Requirement</span></span> | <span data-ttu-id="37508-136">Value</span><span class="sxs-lookup"><span data-stu-id="37508-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37508-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37508-137">Minimum supported client</span></span><br/> | <span data-ttu-id="37508-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="37508-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="37508-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37508-139">Minimum supported server</span></span><br/> | <span data-ttu-id="37508-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37508-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="37508-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="37508-141">End of client support</span></span><br/>    | <span data-ttu-id="37508-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37508-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="37508-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="37508-143">End of server support</span></span><br/>    | <span data-ttu-id="37508-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37508-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="37508-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="37508-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37508-146">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="37508-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="37508-147">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="37508-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
