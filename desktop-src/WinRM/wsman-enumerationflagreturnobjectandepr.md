---
title: Método WSMan. EnumerationFlagReturnObjectAndEPR (WSManDisp. h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagReturnObjectAndEPR para su uso en el parámetro flags de Session. Enumerate.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnObjectAndEPR Administración remota de Windows
- Administración remota de Windows método EnumerationFlagReturnObjectAndEPR, objeto WSMan
- Administración remota de Windows de objeto WSMan, método EnumerationFlagReturnObjectAndEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187f8c029d0392ad9ac1a909e1e45de165815e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492550"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a><span data-ttu-id="b04f2-106">WSMan. EnumerationFlagReturnObjectAndEPR (método)</span><span class="sxs-lookup"><span data-stu-id="b04f2-106">WSMan.EnumerationFlagReturnObjectAndEPR method</span></span>

<span data-ttu-id="b04f2-107">El método **EnumerationFlagReturnObjectAndEPR** devuelve el valor de la marca de enumeración **EnumerationFlagReturnObjectAndEPR** para su uso en el parámetro *Flags* de [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="b04f2-107">The **EnumerationFlagReturnObjectAndEPR** method returns the value of the enumeration flag **EnumerationFlagReturnObjectAndEPR** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="b04f2-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="b04f2-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="b04f2-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b04f2-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="b04f2-110">**EnumerationFlagReturnObjectAndEPR** es una constante de la enumeración **\_ WSManEnumFlags** y se describe en [**constantes de enumeración**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b04f2-110">**EnumerationFlagReturnObjectAndEPR** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b04f2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b04f2-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="b04f2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b04f2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04f2-113">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b04f2-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b04f2-114">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="b04f2-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04f2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b04f2-115">Return value</span></span>

<span data-ttu-id="b04f2-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b04f2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b04f2-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b04f2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b04f2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b04f2-118">Requirements</span></span>



| <span data-ttu-id="b04f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b04f2-119">Requirement</span></span> | <span data-ttu-id="b04f2-120">Value</span><span class="sxs-lookup"><span data-stu-id="b04f2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04f2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b04f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b04f2-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b04f2-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b04f2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b04f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b04f2-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b04f2-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b04f2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b04f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04f2-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04f2-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b04f2-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b04f2-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b04f2-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b04f2-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b04f2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b04f2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b04f2-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b04f2-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b04f2-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b04f2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b04f2-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b04f2-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b04f2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b04f2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04f2-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="b04f2-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="b04f2-135">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="b04f2-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





