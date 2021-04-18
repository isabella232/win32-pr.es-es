---
description: Comprueba si un generador se debe asociar a una propiedad determinada.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'IProvidePropertyBuilder:: MapPropertyToBuilder (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670522"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="39159-103">IProvidePropertyBuilder:: MapPropertyToBuilder (método)</span><span class="sxs-lookup"><span data-stu-id="39159-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="39159-104">Comprueba si un generador se debe asociar a una propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="39159-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="39159-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39159-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="39159-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39159-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39159-107">*DISPID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39159-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39159-108">DISPID de la propiedad en cuestión.</span><span class="sxs-lookup"><span data-stu-id="39159-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="39159-109">*pdwCtlBldType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39159-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39159-110">Generador que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="39159-110">The builder to be mapped.</span></span> <span data-ttu-id="39159-111">Este parámetro puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="39159-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="39159-112">Value</span><span class="sxs-lookup"><span data-stu-id="39159-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="39159-113">Significado</span><span class="sxs-lookup"><span data-stu-id="39159-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="39159-114"><dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="39159-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="39159-115">Invocar un generador de sistema estándar (no compatible con Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="39159-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="39159-116"><dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="39159-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="39159-117">Invoca un generador personalizado.</span><span class="sxs-lookup"><span data-stu-id="39159-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="39159-118"><dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="39159-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="39159-119">El compilador modifica el objeto.</span><span class="sxs-lookup"><span data-stu-id="39159-119">Builder modifies the object.</span></span> <span data-ttu-id="39159-120">Se trata de un comportamiento normal.</span><span class="sxs-lookup"><span data-stu-id="39159-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="39159-121">*pbstrGuidBldr* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39159-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39159-122">GUID que identifica el generador para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="39159-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="39159-123">*builderAvailable* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="39159-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="39159-124">Este parámetro es **true** si esta propiedad admite actualmente un generador.</span><span class="sxs-lookup"><span data-stu-id="39159-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39159-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39159-125">Return value</span></span>

<span data-ttu-id="39159-126">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39159-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="39159-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39159-127">Requirements</span></span>



| <span data-ttu-id="39159-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="39159-128">Requirement</span></span> | <span data-ttu-id="39159-129">Value</span><span class="sxs-lookup"><span data-stu-id="39159-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39159-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39159-130">DLL</span></span><br/> | <dl> <span data-ttu-id="39159-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39159-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39159-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="39159-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39159-133">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="39159-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




