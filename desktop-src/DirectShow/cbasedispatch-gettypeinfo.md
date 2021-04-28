---
description: 'Método CBaseDispatch.GetTypeInfo: el método GetTypeInfo recupera la información de tipo del objeto , que se puede usar para obtener la información de tipo de una interfaz.'
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120123"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="793e4-103">Método CBaseDispatch.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="793e4-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="793e4-104">El método recupera la información de tipo del objeto , que luego se `GetTypeInfo` puede usar para obtener la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="793e4-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="793e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="793e4-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="793e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="793e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="793e4-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="793e4-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="793e4-108">Referencia a un identificador de interfaz (IID) que especifica la interfaz.</span><span class="sxs-lookup"><span data-stu-id="793e4-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="793e4-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="793e4-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="793e4-110">Escriba la información que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="793e4-110">Type information to return.</span></span> <span data-ttu-id="793e4-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="793e4-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="793e4-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="793e4-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="793e4-113">Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="793e4-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="793e4-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="793e4-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="793e4-115">Dirección de una variable que recibe un **puntero ITypeInfo.**</span><span class="sxs-lookup"><span data-stu-id="793e4-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="793e4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="793e4-116">Return value</span></span>

<span data-ttu-id="793e4-117">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="793e4-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="793e4-118">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="793e4-118">Possible values include the following.</span></span>



| <span data-ttu-id="793e4-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="793e4-119">Return code</span></span>                                                                                             | <span data-ttu-id="793e4-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="793e4-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="793e4-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="793e4-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="793e4-122">Correcto.</span><span class="sxs-lookup"><span data-stu-id="793e4-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="793e4-123"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="793e4-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="793e4-124">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="793e4-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="793e4-125"><dt>**TYPE \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="793e4-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="793e4-126">El *parámetro itinfo* no es cero.</span><span class="sxs-lookup"><span data-stu-id="793e4-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="793e4-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="793e4-127">Remarks</span></span>

<span data-ttu-id="793e4-128">Este método se comporta como el **método IDispatch::GetTypeInfo.**</span><span class="sxs-lookup"><span data-stu-id="793e4-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="793e4-129">Sin embargo, incluye un parámetro adicional, *riid*, que especifica la interfaz para la que se va a recuperar información de tipo.</span><span class="sxs-lookup"><span data-stu-id="793e4-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="793e4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="793e4-130">Requirements</span></span>



| <span data-ttu-id="793e4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="793e4-131">Requirement</span></span> | <span data-ttu-id="793e4-132">Value</span><span class="sxs-lookup"><span data-stu-id="793e4-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="793e4-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="793e4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="793e4-134"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="793e4-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="793e4-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="793e4-135">Library</span></span><br/> | <dl> <span data-ttu-id="793e4-136"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="793e4-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793e4-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="793e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793e4-138">**CBaseDispatch (clase)**</span><span class="sxs-lookup"><span data-stu-id="793e4-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




