---
title: Método WSMan. SessionFlagSkipCNCheck (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagSkipCNCheck para su uso en el parámetro flags de WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Método SessionFlagSkipCNCheck Administración remota de Windows
- Administración remota de Windows método SessionFlagSkipCNCheck, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagSkipCNCheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996668"
---
# <a name="wsmansessionflagskipcncheck-method"></a><span data-ttu-id="53305-106">WSMan. SessionFlagSkipCNCheck (método)</span><span class="sxs-lookup"><span data-stu-id="53305-106">WSMan.SessionFlagSkipCNCheck method</span></span>

<span data-ttu-id="53305-107">El método **WSMan. SessionFlagSkipCNCheck** devuelve el valor de la marca de autenticación **WSManFlagSkipCNCheck** para su uso en el parámetro *Flags* de [**WSMan. createSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="53305-107">The **WSMan.SessionFlagSkipCNCheck** method returns the value of the **WSManFlagSkipCNCheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="53305-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="53305-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="53305-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="53305-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="53305-110">**WSManFlagSkipCNCheck** es una constante de la enumeración **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="53305-110">**WSManFlagSkipCNCheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="53305-111">Para obtener más información, consulte [**constantes de autenticación**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="53305-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="53305-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53305-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="53305-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53305-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53305-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53305-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53305-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="53305-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53305-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53305-116">Return value</span></span>

<span data-ttu-id="53305-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="53305-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53305-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53305-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53305-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53305-119">Requirements</span></span>



| <span data-ttu-id="53305-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53305-120">Requirement</span></span> | <span data-ttu-id="53305-121">Value</span><span class="sxs-lookup"><span data-stu-id="53305-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53305-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53305-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53305-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53305-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="53305-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53305-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53305-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53305-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="53305-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53305-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="53305-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="53305-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="53305-128">IDL</span><span class="sxs-lookup"><span data-stu-id="53305-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53305-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53305-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="53305-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53305-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="53305-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="53305-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="53305-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53305-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53305-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53305-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53305-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="53305-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53305-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="53305-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="53305-136">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="53305-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





