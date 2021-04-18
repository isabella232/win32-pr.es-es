---
description: 'El método FreeProps libera los recursos asignados por el método IPropertySetter:: GetProps. Llame a este método después de llamar a GetProps, pasándole las estructuras devueltas por GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'IPropertySetter:: FreeProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679119"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="a9f97-104">IPropertySetter:: FreeProps (método)</span><span class="sxs-lookup"><span data-stu-id="a9f97-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="a9f97-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a9f97-105">\[Deprecated.</span></span> <span data-ttu-id="a9f97-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9f97-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9f97-107">El `FreeProps` método libera los recursos asignados por el método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f97-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="a9f97-108">Llame a este método después de llamar a **GetProps**, pasándole las estructuras devueltas por **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="a9f97-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f97-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9f97-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="a9f97-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9f97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f97-111">*cParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f97-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f97-112">Número de elementos de la matriz de *paparam* .</span><span class="sxs-lookup"><span data-stu-id="a9f97-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="a9f97-113">*param* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f97-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f97-114">Puntero a una matriz de estructuras de [**\_ parámetros de Dexterity**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f97-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="a9f97-115">*Pavalue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f97-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f97-116">Puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f97-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f97-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9f97-117">Return value</span></span>

<span data-ttu-id="a9f97-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a9f97-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9f97-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9f97-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9f97-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a9f97-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9f97-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9f97-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9f97-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a9f97-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9f97-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9f97-123">Requirements</span></span>



| <span data-ttu-id="a9f97-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9f97-124">Requirement</span></span> | <span data-ttu-id="a9f97-125">Value</span><span class="sxs-lookup"><span data-stu-id="a9f97-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f97-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9f97-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a9f97-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f97-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9f97-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9f97-128">Library</span></span><br/> | <dl> <span data-ttu-id="a9f97-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9f97-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9f97-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9f97-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f97-131">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="a9f97-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="a9f97-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a9f97-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




