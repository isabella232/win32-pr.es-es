---
description: El método GetChallenge devuelve un desafío de la tarjeta inteligente.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'ISCardAuth:: GetChallenge (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275915"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="3df3f-103">ISCardAuth:: GetChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="3df3f-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="3df3f-104">\[El método **GetChallenge** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3df3f-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3df3f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3df3f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3df3f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3df3f-107">El método **GetChallenge** devuelve un desafío de la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3df3f-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3df3f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3df3f-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3df3f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3df3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df3f-110">*lAlgoID* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3df3f-111">Algoritmo que se va a usar en el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="3df3f-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="3df3f-112">*lLengthOfChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df3f-113">Longitud máxima de la respuesta esperada.</span><span class="sxs-lookup"><span data-stu-id="3df3f-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="3df3f-114">*pParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df3f-115">Un objeto [**IByteBuffer**](ibytebuffer.md) que contiene los parámetros específicos del proveedor del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="3df3f-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="3df3f-116">*pBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3df3f-117">En la entrada, apunta al búfer.</span><span class="sxs-lookup"><span data-stu-id="3df3f-117">On input, points to the buffer.</span></span>

<span data-ttu-id="3df3f-118">En la salida, contiene los datos de desafío de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="3df3f-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df3f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3df3f-119">Return value</span></span>

<span data-ttu-id="3df3f-120">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3df3f-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3df3f-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3df3f-121">Return code</span></span>                                                                                   | <span data-ttu-id="3df3f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3df3f-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3df3f-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3df3f-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3df3f-124">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="3df3f-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3df3f-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3df3f-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3df3f-126">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="3df3f-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3df3f-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3df3f-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3df3f-128">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="3df3f-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3df3f-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3df3f-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3df3f-130">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="3df3f-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3df3f-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3df3f-131">Remarks</span></span>

<span data-ttu-id="3df3f-132">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="3df3f-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="3df3f-133">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3df3f-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3df3f-134">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3df3f-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3df3f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df3f-135">Requirements</span></span>



| <span data-ttu-id="3df3f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df3f-136">Requirement</span></span> | <span data-ttu-id="3df3f-137">Value</span><span class="sxs-lookup"><span data-stu-id="3df3f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3df3f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3df3f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3df3f-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3df3f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3df3f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3df3f-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3df3f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3df3f-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3df3f-142">End of client support</span></span><br/>    | <span data-ttu-id="3df3f-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3df3f-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3df3f-144">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3df3f-144">End of server support</span></span><br/>    | <span data-ttu-id="3df3f-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3df3f-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3df3f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="3df3f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df3f-147">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="3df3f-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
