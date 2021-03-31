---
title: Método WSMan. SessionFlagUTF8 (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUTF8 para su uso en el parámetro flags de WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUTF8 Administración remota de Windows
- Administración remota de Windows método SessionFlagUTF8, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803560"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="9d847-106">WSMan. SessionFlagUTF8 (método)</span><span class="sxs-lookup"><span data-stu-id="9d847-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="9d847-107">El método **WSMan. SessionFlagUTF8** devuelve el valor de la marca de autenticación **WSManFlagUTF8** para su uso en el parámetro *Flags* de [**WSMan. createSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="9d847-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="9d847-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="9d847-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="9d847-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9d847-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="9d847-110">**WSManFlagUTF8** es una constante de la enumeración **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="9d847-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="9d847-111">Para obtener más información, vea [otras constantes de sesión](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9d847-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d847-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d847-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="9d847-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d847-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d847-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9d847-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d847-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="9d847-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d847-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d847-116">Return value</span></span>

<span data-ttu-id="9d847-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9d847-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d847-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d847-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d847-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d847-119">Requirements</span></span>



| <span data-ttu-id="9d847-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d847-120">Requirement</span></span> | <span data-ttu-id="9d847-121">Value</span><span class="sxs-lookup"><span data-stu-id="9d847-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d847-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d847-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9d847-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d847-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9d847-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d847-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9d847-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d847-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9d847-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d847-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d847-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d847-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d847-128">IDL</span><span class="sxs-lookup"><span data-stu-id="9d847-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d847-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d847-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d847-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d847-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d847-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9d847-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9d847-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d847-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d847-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d847-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d847-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d847-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d847-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="9d847-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="9d847-136">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="9d847-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





