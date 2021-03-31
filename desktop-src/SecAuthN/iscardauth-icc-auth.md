---
description: El método de autenticación de ICC \_ permite que una aplicación autentique la tarjeta inteligente.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'ISCardAuth:: ICC_Auth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001090"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="5bc1b-103">ISCardAuth:: ICC ( \_ método de autenticación)</span><span class="sxs-lookup"><span data-stu-id="5bc1b-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="5bc1b-104">\[El método de **\_ autenticación de ICC** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5bc1b-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5bc1b-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5bc1b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5bc1b-107">El método de **\_ autenticación de ICC** permite que una aplicación autentique la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc1b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bc1b-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5bc1b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bc1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc1b-110">*lAlgoID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bc1b-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc1b-111">Algoritmo que se va a usar en el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="5bc1b-112">*pParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bc1b-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc1b-113">Un objeto [**IByteBuffer**](ibytebuffer.md) que contiene los parámetros específicos del proveedor del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="5bc1b-114">*pBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5bc1b-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc1b-115">En la entrada, contiene los datos que se van a usar en el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="5bc1b-116">En la salida, contiene el resultado del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc1b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bc1b-117">Return value</span></span>

<span data-ttu-id="5bc1b-118">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5bc1b-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5bc1b-119">Return code</span></span>                                                                                   | <span data-ttu-id="5bc1b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bc1b-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5bc1b-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1b-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5bc1b-122">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="5bc1b-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1b-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5bc1b-124">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="5bc1b-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1b-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5bc1b-126">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="5bc1b-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1b-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5bc1b-128">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="5bc1b-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="5bc1b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bc1b-129">Remarks</span></span>

<span data-ttu-id="5bc1b-130">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1b-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="5bc1b-131">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5bc1b-132">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1b-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc1b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc1b-133">Requirements</span></span>



| <span data-ttu-id="5bc1b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc1b-134">Requirement</span></span> | <span data-ttu-id="5bc1b-135">Value</span><span class="sxs-lookup"><span data-stu-id="5bc1b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5bc1b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bc1b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc1b-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5bc1b-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5bc1b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bc1b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc1b-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5bc1b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5bc1b-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5bc1b-140">End of client support</span></span><br/>    | <span data-ttu-id="5bc1b-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5bc1b-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="5bc1b-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5bc1b-142">End of server support</span></span><br/>    | <span data-ttu-id="5bc1b-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5bc1b-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="5bc1b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bc1b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc1b-145">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="5bc1b-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
