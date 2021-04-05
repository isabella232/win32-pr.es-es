---
title: Método WSMan. SessionFlagUseKerberos (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseKerberos para su uso en el parámetro flags de WSMan. CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseKerberos Administración remota de Windows
- Administración remota de Windows método SessionFlagUseKerberos, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUseKerberos
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e7436a5b79480b39c093545a0b579da3d13082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802365"
---
# <a name="wsmansessionflagusekerberos-method"></a><span data-ttu-id="c278a-106">WSMan. SessionFlagUseKerberos (método)</span><span class="sxs-lookup"><span data-stu-id="c278a-106">WSMan.SessionFlagUseKerberos method</span></span>

<span data-ttu-id="c278a-107">El método **WSMan. SessionFlagUseKerberos** devuelve el valor de la marca de autenticación **WSManFlagUseKerberos** para su uso en el parámetro *Flags* de [**WSMan. createSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="c278a-107">The **WSMan.SessionFlagUseKerberos** method returns the value of the **WSManFlagUseKerberos** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="c278a-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="c278a-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="c278a-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c278a-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="c278a-110">**WSManFlagUseKerberos** es una constante de la enumeración **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="c278a-110">**WSManFlagUseKerberos** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="c278a-111">Para obtener más información, consulte [constantes de autenticación](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c278a-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c278a-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c278a-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseKerberos( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c278a-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c278a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c278a-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c278a-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c278a-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="c278a-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c278a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c278a-116">Return value</span></span>

<span data-ttu-id="c278a-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c278a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c278a-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c278a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c278a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c278a-119">Requirements</span></span>



| <span data-ttu-id="c278a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c278a-120">Requirement</span></span> | <span data-ttu-id="c278a-121">Value</span><span class="sxs-lookup"><span data-stu-id="c278a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c278a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c278a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c278a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c278a-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c278a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c278a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c278a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c278a-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c278a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c278a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c278a-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c278a-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c278a-128">IDL</span><span class="sxs-lookup"><span data-stu-id="c278a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c278a-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c278a-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c278a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c278a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c278a-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c278a-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c278a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c278a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c278a-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c278a-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c278a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c278a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c278a-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="c278a-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c278a-136">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="c278a-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





