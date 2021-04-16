---
description: Notifica a un objeto que debe mostrar su generador para la propiedad especificada.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'IProvidePropertyBuilder:: ExecuteBuilder (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649567"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="bc753-103">IProvidePropertyBuilder:: ExecuteBuilder (método)</span><span class="sxs-lookup"><span data-stu-id="bc753-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="bc753-104">Notifica a un objeto que debe mostrar su generador para la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="bc753-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc753-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc753-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="bc753-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc753-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc753-107">*DISPID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc753-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc753-108">El DISPID de la propiedad que muestra el generador.</span><span class="sxs-lookup"><span data-stu-id="bc753-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="bc753-109">*bstrGuidBldr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc753-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc753-110">**BSTR** del GUID del compilador que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="bc753-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="bc753-111">Se devuelve desde [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="bc753-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc753-112">*pdispApp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc753-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc753-113">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="bc753-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc753-114">*hwndBldrOwner* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc753-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc753-115">Identificador de la ventana primaria del generador emergente.</span><span class="sxs-lookup"><span data-stu-id="bc753-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="bc753-116">*pvarValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc753-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc753-117">El valor actual de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bc753-117">The current value of the property.</span></span> <span data-ttu-id="bc753-118">Este valor puede ser modificado por el objeto y cambia al nuevo valor si *pbActionCommitted* es **true**.</span><span class="sxs-lookup"><span data-stu-id="bc753-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="bc753-119">*pbActionCommitted* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bc753-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bc753-120">Valor que indica si el generador realizó una acción en el objeto.</span><span class="sxs-lookup"><span data-stu-id="bc753-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="bc753-121">Se puede usar cuando un usuario modifica algo y, a continuación, presiona aceptar en el cuadro de diálogo Generador emergente.</span><span class="sxs-lookup"><span data-stu-id="bc753-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc753-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc753-122">Return value</span></span>

<span data-ttu-id="bc753-123">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc753-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc753-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc753-124">Requirements</span></span>



| <span data-ttu-id="bc753-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc753-125">Requirement</span></span> | <span data-ttu-id="bc753-126">Value</span><span class="sxs-lookup"><span data-stu-id="bc753-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc753-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc753-127">DLL</span></span><br/> | <dl> <span data-ttu-id="bc753-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc753-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc753-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc753-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc753-130">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="bc753-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




