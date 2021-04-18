---
title: Método WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseCredSsp para su uso en el parámetro flags del método WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseCredSsp Administración remota de Windows
- Administración remota de Windows método SessionFlagUseCredSsp, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490756"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="52233-106">WSMan. SessionFlagUseCredSsp (método)</span><span class="sxs-lookup"><span data-stu-id="52233-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="52233-107">Devuelve el valor de la marca de autenticación **WSManFlagUseCredSsp** para su uso en el parámetro *Flags* del método [**WSMan. createSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="52233-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="52233-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="52233-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="52233-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="52233-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="52233-110">**WSManFlagUseCredSsp** es una constante de la enumeración **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="52233-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="52233-111">Para obtener más información, consulte [constantes de autenticación](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="52233-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="52233-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52233-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="52233-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52233-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52233-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="52233-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52233-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="52233-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52233-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52233-116">Return value</span></span>

<span data-ttu-id="52233-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="52233-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52233-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52233-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="52233-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52233-119">Requirements</span></span>



| <span data-ttu-id="52233-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="52233-120">Requirement</span></span> | <span data-ttu-id="52233-121">Value</span><span class="sxs-lookup"><span data-stu-id="52233-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52233-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52233-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52233-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52233-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="52233-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52233-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52233-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52233-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="52233-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="52233-126">Redistributable</span></span><br/>          | <span data-ttu-id="52233-127">Windows Management Framework en Windows Server 2008 con SP2, Windows Vista con SP1 y Windows Vista con SP2</span><span class="sxs-lookup"><span data-stu-id="52233-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="52233-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52233-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="52233-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="52233-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="52233-130">IDL</span><span class="sxs-lookup"><span data-stu-id="52233-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52233-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52233-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="52233-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52233-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="52233-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52233-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="52233-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52233-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52233-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52233-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="52233-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="52233-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52233-137">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="52233-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="52233-138">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="52233-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





