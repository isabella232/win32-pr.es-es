---
description: Reemplaza el código CHV actual (verificación del titular de la tarjeta) por el nuevo código CHV.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'ISCardVerify:: ChangeCode (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814382"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="cd2bd-103">ISCardVerify:: ChangeCode (método)</span><span class="sxs-lookup"><span data-stu-id="cd2bd-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="cd2bd-104">\[El método **ChangeCode** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd2bd-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd2bd-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cd2bd-107">El método **ChangeCode** reemplaza el código CHV actual (verificación del titular de la tarjeta) con el nuevo código CHV.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2bd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd2bd-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="cd2bd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd2bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd2bd-110">*pOldCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2bd-111">Puntero a un [**IByteBuffer**](ibytebuffer.md) que contiene el código actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="cd2bd-112">*pNewCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2bd-113">Puntero a un [**IByteBuffer**](ibytebuffer.md) que contiene el nuevo código que se presentará a la [*tarjeta inteligente*](../secgloss/s-gly.md) durante el proceso de cambio para autenticar al usuario.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="cd2bd-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2bd-115">Indica si el código es global o local, y si el código debe estar habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="cd2bd-116">**SC \_ FL \_ \_ global**</span><span class="sxs-lookup"><span data-stu-id="cd2bd-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="cd2bd-117">**SC \_ FL \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="cd2bd-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="cd2bd-118">**\_ \_ Habilitar IHV de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="cd2bd-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="cd2bd-119">**deshabilitar IHV de SC \_ FL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd2bd-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="cd2bd-120">*lRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2bd-121">Referencia específica de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd2bd-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd2bd-122">Return value</span></span>

<span data-ttu-id="cd2bd-123">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="cd2bd-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="cd2bd-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cd2bd-124">Return code</span></span>                                                                                   | <span data-ttu-id="cd2bd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd2bd-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cd2bd-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cd2bd-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cd2bd-127">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cd2bd-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cd2bd-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cd2bd-129">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="cd2bd-130"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="cd2bd-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cd2bd-131">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="cd2bd-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cd2bd-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cd2bd-133">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="cd2bd-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="cd2bd-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd2bd-134">Remarks</span></span>

<span data-ttu-id="cd2bd-135">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="cd2bd-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="cd2bd-136">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd2bd-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cd2bd-137">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cd2bd-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2bd-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd2bd-138">Requirements</span></span>



| <span data-ttu-id="cd2bd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd2bd-139">Requirement</span></span> | <span data-ttu-id="cd2bd-140">Value</span><span class="sxs-lookup"><span data-stu-id="cd2bd-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd2bd-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd2bd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2bd-142">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cd2bd-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd2bd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2bd-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd2bd-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cd2bd-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="cd2bd-145">End of client support</span></span><br/>    | <span data-ttu-id="cd2bd-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd2bd-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="cd2bd-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="cd2bd-147">End of server support</span></span><br/>    | <span data-ttu-id="cd2bd-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd2bd-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="cd2bd-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd2bd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2bd-150">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd2bd-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="cd2bd-151">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="cd2bd-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="cd2bd-152">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="cd2bd-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
