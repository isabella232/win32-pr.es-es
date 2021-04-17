---
title: Método WSMan. EnumerationFlagHierarchyDeepBasePropsOnly (WSManDisp. h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagHierarchyDeepBasePropsOnly para su uso en el parámetro flags de Session. Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagHierarchyDeepBasePropsOnly Administración remota de Windows
- Administración remota de Windows método EnumerationFlagHierarchyDeepBasePropsOnly, objeto WSMan
- Administración remota de Windows de objeto WSMan, método EnumerationFlagHierarchyDeepBasePropsOnly
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a0ed7d725f60e673d3426be1b11179ec8333d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714583"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a><span data-ttu-id="3eb7c-106">WSMan. EnumerationFlagHierarchyDeepBasePropsOnly (método)</span><span class="sxs-lookup"><span data-stu-id="3eb7c-106">WSMan.EnumerationFlagHierarchyDeepBasePropsOnly method</span></span>

<span data-ttu-id="3eb7c-107">El método **WSMan. EnumerationFlagHierarchyDeepBasePropsOnly** devuelve el valor de la marca de enumeración **EnumerationFlagHierarchyDeepBasePropsOnly** para su uso en el parámetro *Flags* de [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="3eb7c-107">The **WSMan.EnumerationFlagHierarchyDeepBasePropsOnly** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeepBasePropsOnly** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="3eb7c-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="3eb7c-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="3eb7c-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3eb7c-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="3eb7c-110">**EnumerationFlagHierarchyDeepBasePropsOnly** es una constante de la enumeración **\_ WSManEnumFlags** y se describe en [**constantes de enumeración**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3eb7c-110">**EnumerationFlagHierarchyDeepBasePropsOnly** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb7c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3eb7c-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="3eb7c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3eb7c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eb7c-113">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3eb7c-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb7c-114">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="3eb7c-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eb7c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3eb7c-115">Return value</span></span>

<span data-ttu-id="3eb7c-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3eb7c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3eb7c-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3eb7c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eb7c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eb7c-118">Requirements</span></span>



| <span data-ttu-id="3eb7c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eb7c-119">Requirement</span></span> | <span data-ttu-id="3eb7c-120">Value</span><span class="sxs-lookup"><span data-stu-id="3eb7c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb7c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3eb7c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb7c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eb7c-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3eb7c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3eb7c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb7c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3eb7c-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3eb7c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3eb7c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eb7c-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eb7c-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3eb7c-127">IDL</span><span class="sxs-lookup"><span data-stu-id="3eb7c-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3eb7c-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3eb7c-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3eb7c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3eb7c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3eb7c-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3eb7c-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3eb7c-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3eb7c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eb7c-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eb7c-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3eb7c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3eb7c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb7c-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="3eb7c-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="3eb7c-135">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="3eb7c-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





