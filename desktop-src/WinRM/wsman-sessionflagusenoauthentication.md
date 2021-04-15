---
title: Método WSMan. SessionFlagUseNoAuthentication (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseNoAuthentication para su uso en el parámetro flags del método WSMan. CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseNoAuthentication Administración remota de Windows
- Administración remota de Windows método SessionFlagUseNoAuthentication, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUseNoAuthentication
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9676d3baa9a18ae8a3feb5eb4092c63586a94b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492670"
---
# <a name="wsmansessionflagusenoauthentication-method"></a><span data-ttu-id="5dffe-106">WSMan. SessionFlagUseNoAuthentication (método)</span><span class="sxs-lookup"><span data-stu-id="5dffe-106">WSMan.SessionFlagUseNoAuthentication method</span></span>

<span data-ttu-id="5dffe-107">El método **wsman. SessionFlagUseNoAuthentication** devuelve el valor de la marca de autenticación **WSManFlagUseNoAuthentication** para su uso en el parámetro *Flags* del método [**WSMan. createSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="5dffe-107">The **WSMan.SessionFlagUseNoAuthentication** method returns the value of the **WSManFlagUseNoAuthentication** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="5dffe-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="5dffe-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="5dffe-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5dffe-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="5dffe-110">**WSManFlagUseNoAuthentication** es una constante de la enumeración **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="5dffe-110">**WSManFlagUseNoAuthentication** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="5dffe-111">Para obtener más información, vea//[constantes de autenticación](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5dffe-111">For more information, see //[Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dffe-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dffe-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNoAuthentication( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="5dffe-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dffe-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dffe-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5dffe-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dffe-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="5dffe-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dffe-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dffe-116">Return value</span></span>

<span data-ttu-id="5dffe-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5dffe-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5dffe-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5dffe-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dffe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dffe-119">Requirements</span></span>



| <span data-ttu-id="5dffe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dffe-120">Requirement</span></span> | <span data-ttu-id="5dffe-121">Value</span><span class="sxs-lookup"><span data-stu-id="5dffe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dffe-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dffe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5dffe-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dffe-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5dffe-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dffe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5dffe-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dffe-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5dffe-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dffe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dffe-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dffe-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dffe-128">IDL</span><span class="sxs-lookup"><span data-stu-id="5dffe-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5dffe-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5dffe-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5dffe-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dffe-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dffe-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5dffe-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5dffe-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5dffe-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dffe-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dffe-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5dffe-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dffe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dffe-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="5dffe-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="5dffe-136">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="5dffe-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





