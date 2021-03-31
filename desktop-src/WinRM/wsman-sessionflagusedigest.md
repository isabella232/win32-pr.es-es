---
title: Método WSMan. SessionFlagUseDigest (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseDigest para su uso en el parámetro flags del método WSMan. CreateSession.
ms.assetid: dba2448a-4f72-4000-8687-4c1be812fc3b
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseDigest Administración remota de Windows
- Administración remota de Windows método SessionFlagUseDigest, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUseDigest
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseDigest
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4018428123443836c4f433f3e82f03a93ee9b766
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079410"
---
# <a name="wsmansessionflagusedigest-method"></a><span data-ttu-id="18dc3-106">WSMan. SessionFlagUseDigest (método)</span><span class="sxs-lookup"><span data-stu-id="18dc3-106">WSMan.SessionFlagUseDigest method</span></span>

<span data-ttu-id="18dc3-107">El método **wsman. SessionFlagUseDigest** devuelve el valor de la marca de autenticación **WSManFlagUseDigest** para su uso en el parámetro *Flags* del método [**WSMan. createSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="18dc3-107">The **WSMan.SessionFlagUseDigest** method returns the value of the **WSManFlagUseDigest** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="18dc3-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="18dc3-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="18dc3-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="18dc3-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="18dc3-110">**WSManFlagUseDigest** es un valor de la enumeración **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="18dc3-110">**WSManFlagUseDigest** is a value in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="18dc3-111">Para obtener más información, consulte [constantes de autenticación](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="18dc3-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="18dc3-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18dc3-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseDigest( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="18dc3-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18dc3-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18dc3-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18dc3-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18dc3-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="18dc3-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18dc3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18dc3-116">Return value</span></span>

<span data-ttu-id="18dc3-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="18dc3-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18dc3-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18dc3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="18dc3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18dc3-119">Requirements</span></span>



| <span data-ttu-id="18dc3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="18dc3-120">Requirement</span></span> | <span data-ttu-id="18dc3-121">Value</span><span class="sxs-lookup"><span data-stu-id="18dc3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18dc3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18dc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="18dc3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18dc3-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="18dc3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18dc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="18dc3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18dc3-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="18dc3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18dc3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="18dc3-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18dc3-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="18dc3-128">IDL</span><span class="sxs-lookup"><span data-stu-id="18dc3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18dc3-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18dc3-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="18dc3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18dc3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="18dc3-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="18dc3-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="18dc3-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18dc3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18dc3-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18dc3-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18dc3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="18dc3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18dc3-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="18dc3-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="18dc3-136">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="18dc3-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





