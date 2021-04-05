---
title: Método WSMan. EnumerationFlagNonXmlText (WSManDisp. h)
description: Devuelve el valor de la constante de enumeración WSManFlagNonXmlText para su uso en el parámetro flags del método Session. Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagNonXmlText Administración remota de Windows
- Administración remota de Windows método EnumerationFlagNonXmlText, objeto WSMan
- Administración remota de Windows de objeto WSMan, método EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802918"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="a831b-106">WSMan. EnumerationFlagNonXmlText (método)</span><span class="sxs-lookup"><span data-stu-id="a831b-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="a831b-107">**WSMan. EnumerationFlagNonXmlText** devuelve el valor de la constante de enumeración **WSManFlagNonXmlText** para su uso en el parámetro *Flags* del método [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="a831b-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="a831b-108">Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante.</span><span class="sxs-lookup"><span data-stu-id="a831b-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="a831b-109">Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a831b-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="a831b-110">**WSManFlagNonXmlText** es una constante de la enumeración **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="a831b-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="a831b-111">Para obtener más información, vea [**constantes de enumeración**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a831b-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a831b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a831b-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="a831b-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a831b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a831b-114">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a831b-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a831b-115">Valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="a831b-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a831b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a831b-116">Return value</span></span>

<span data-ttu-id="a831b-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a831b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a831b-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a831b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a831b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a831b-119">Requirements</span></span>



| <span data-ttu-id="a831b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a831b-120">Requirement</span></span> | <span data-ttu-id="a831b-121">Value</span><span class="sxs-lookup"><span data-stu-id="a831b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a831b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a831b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a831b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a831b-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a831b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a831b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a831b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a831b-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a831b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a831b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a831b-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a831b-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a831b-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a831b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a831b-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a831b-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a831b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a831b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a831b-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a831b-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a831b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a831b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a831b-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a831b-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a831b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a831b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a831b-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="a831b-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="a831b-136">**IWSManEx**</span><span class="sxs-lookup"><span data-stu-id="a831b-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="a831b-137">**IWSManSession**</span><span class="sxs-lookup"><span data-stu-id="a831b-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





