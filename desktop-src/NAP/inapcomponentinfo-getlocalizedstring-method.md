---
title: Método INapComponentInfo GetLocalizedString (NapCommon. h)
description: Lo usa el sistema NAP para obtener cadenas traducidas.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Método GetLocalizedString NAP
- Método GetLocalizedString NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997156"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="038cb-106">INapComponentInfo:: GetLocalizedString (método)</span><span class="sxs-lookup"><span data-stu-id="038cb-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="038cb-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="038cb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="038cb-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetLocalizedString** para obtener cadenas localizadas.</span><span class="sxs-lookup"><span data-stu-id="038cb-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="038cb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="038cb-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="038cb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="038cb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038cb-111">*msgId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="038cb-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="038cb-112">[**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la cadena que se va a localizar.</span><span class="sxs-lookup"><span data-stu-id="038cb-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="038cb-113">*cadena* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="038cb-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="038cb-114">Un puntero a un puntero a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión localizada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="038cb-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038cb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="038cb-115">Return value</span></span>

<span data-ttu-id="038cb-116">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="038cb-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="038cb-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="038cb-117">Return code</span></span>                                                                                     | <span data-ttu-id="038cb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="038cb-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="038cb-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="038cb-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="038cb-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="038cb-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="038cb-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="038cb-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="038cb-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="038cb-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="038cb-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="038cb-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="038cb-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="038cb-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="038cb-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="038cb-125">Remarks</span></span>

<span data-ttu-id="038cb-126">Las cadenas deben localizarse según el identificador de idioma del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="038cb-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="038cb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="038cb-127">Requirements</span></span>



| <span data-ttu-id="038cb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="038cb-128">Requirement</span></span> | <span data-ttu-id="038cb-129">Value</span><span class="sxs-lookup"><span data-stu-id="038cb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="038cb-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="038cb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="038cb-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="038cb-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="038cb-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="038cb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="038cb-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="038cb-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="038cb-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="038cb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="038cb-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="038cb-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="038cb-136">IDL</span><span class="sxs-lookup"><span data-stu-id="038cb-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="038cb-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="038cb-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038cb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="038cb-138">See also</span></span>

<dl> <span data-ttu-id="038cb-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="038cb-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="038cb-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="038cb-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





