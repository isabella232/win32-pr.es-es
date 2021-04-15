---
title: Método WSMan. EnumerationFlagReturnEPR (WSManDisp. h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagReturnEPR para su uso en el parámetro flags de Session. Enumerate.
ms.assetid: 5e168aa9-5be1-46b3-bb9b-59895e68a75d
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnEPR Administración remota de Windows
- Administración remota de Windows método EnumerationFlagReturnEPR, objeto WSMan
- Administración remota de Windows de objeto WSMan, método EnumerationFlagReturnEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129aca059bcca1b1a6f6729d4df97fbf8617fa52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489106"
---
# <a name="wsmanenumerationflagreturnepr-method"></a><span data-ttu-id="d7289-106">WSMan. EnumerationFlagReturnEPR (método)</span><span class="sxs-lookup"><span data-stu-id="d7289-106">WSMan.EnumerationFlagReturnEPR method</span></span>

<span data-ttu-id="d7289-107">El método **EnumerationFlagReturnEPR** devuelve el valor de la marca de enumeración **EnumerationFlagReturnEPR** para su uso en el parámetro *Flags* de [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="d7289-107">The **EnumerationFlagReturnEPR** method returns the value of the enumeration flag **EnumerationFlagReturnEPR** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="d7289-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="d7289-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="d7289-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d7289-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="d7289-110">**EnumerationFlagReturnEPR** es una constante de la enumeración **\_ WSManEnumFlags** y se describe en [**constantes de enumeración**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d7289-110">**EnumerationFlagReturnEPR** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7289-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7289-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="d7289-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7289-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7289-113">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7289-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7289-114">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="d7289-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7289-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7289-115">Return value</span></span>

<span data-ttu-id="d7289-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d7289-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7289-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7289-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7289-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7289-118">Requirements</span></span>



| <span data-ttu-id="d7289-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7289-119">Requirement</span></span> | <span data-ttu-id="d7289-120">Value</span><span class="sxs-lookup"><span data-stu-id="d7289-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7289-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7289-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7289-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7289-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d7289-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7289-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7289-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7289-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d7289-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7289-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7289-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7289-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7289-127">IDL</span><span class="sxs-lookup"><span data-stu-id="d7289-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7289-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7289-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7289-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7289-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7289-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7289-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7289-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7289-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7289-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7289-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7289-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7289-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7289-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="d7289-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="d7289-135">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="d7289-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





