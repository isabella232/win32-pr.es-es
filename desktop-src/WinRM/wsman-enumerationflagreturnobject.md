---
title: Método WSMan. EnumerationFlagReturnObject (WSManDisp. h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagReturnObject para su uso en el parámetro flags de Session. Enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnObject Administración remota de Windows
- Administración remota de Windows método EnumerationFlagReturnObject, objeto WSMan
- Administración remota de Windows de objeto WSMan, método EnumerationFlagReturnObject
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3019f880503f91d1488a2b7a41574cadc2df987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714613"
---
# <a name="wsmanenumerationflagreturnobject-method"></a><span data-ttu-id="324a9-106">WSMan. EnumerationFlagReturnObject (método)</span><span class="sxs-lookup"><span data-stu-id="324a9-106">WSMan.EnumerationFlagReturnObject method</span></span>

<span data-ttu-id="324a9-107">El método **WSMan. EnumerationFlagReturnObject** devuelve el valor de la marca de enumeración **EnumerationFlagReturnObject** para su uso en el parámetro *Flags* de [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="324a9-107">The **WSMan.EnumerationFlagReturnObject** method returns the value of the enumeration flag **EnumerationFlagReturnObject** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="324a9-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="324a9-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="324a9-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="324a9-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="324a9-110">**EnumerationFlagReturnObject** es una constante de la enumeración **\_ WSManEnumFlags** y se describe en [**constantes de enumeración**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="324a9-110">**EnumerationFlagReturnObject** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="324a9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="324a9-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnObject( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="324a9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="324a9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="324a9-113">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="324a9-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="324a9-114">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="324a9-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="324a9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="324a9-115">Return value</span></span>

<span data-ttu-id="324a9-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="324a9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="324a9-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="324a9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="324a9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="324a9-118">Requirements</span></span>



| <span data-ttu-id="324a9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="324a9-119">Requirement</span></span> | <span data-ttu-id="324a9-120">Value</span><span class="sxs-lookup"><span data-stu-id="324a9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="324a9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="324a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="324a9-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="324a9-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="324a9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="324a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="324a9-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="324a9-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="324a9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="324a9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="324a9-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="324a9-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="324a9-127">IDL</span><span class="sxs-lookup"><span data-stu-id="324a9-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="324a9-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="324a9-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="324a9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="324a9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="324a9-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="324a9-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="324a9-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="324a9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="324a9-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="324a9-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="324a9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="324a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324a9-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="324a9-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="324a9-135">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="324a9-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





