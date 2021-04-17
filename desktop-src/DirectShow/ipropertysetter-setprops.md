---
description: El método SetProps establece las propiedades del objeto de destino en el estado adecuado durante el tiempo especificado.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'IPropertySetter:: SetProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680491"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="aaf28-103">IPropertySetter:: SetProps (método)</span><span class="sxs-lookup"><span data-stu-id="aaf28-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="aaf28-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="aaf28-104">\[Deprecated.</span></span> <span data-ttu-id="aaf28-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aaf28-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aaf28-106">El `SetProps` método establece las propiedades del objeto de destino en el estado adecuado durante el tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="aaf28-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf28-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aaf28-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="aaf28-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aaf28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf28-109">*pTarget* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaf28-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf28-110">Puntero al objeto de destino para el que se van a establecer las propiedades.</span><span class="sxs-lookup"><span data-stu-id="aaf28-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="aaf28-111">*rtNow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaf28-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf28-112">Hora a la que se van a establecer las propiedades, en unidades de 100-nanosegundos, o – 1 para establecer propiedades estáticas (las que no varían con el tiempo).</span><span class="sxs-lookup"><span data-stu-id="aaf28-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf28-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aaf28-113">Return value</span></span>

<span data-ttu-id="aaf28-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="aaf28-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aaf28-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aaf28-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf28-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aaf28-116">Remarks</span></span>

<span data-ttu-id="aaf28-117">DES llama a este método para establecer las propiedades en una transición o efecto.</span><span class="sxs-lookup"><span data-stu-id="aaf28-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="aaf28-118">Normalmente, una aplicación no llamará a este método.</span><span class="sxs-lookup"><span data-stu-id="aaf28-118">An application will not normally call this method.</span></span>

<span data-ttu-id="aaf28-119">El objeto especificado por *pTarget* debe implementar la interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="aaf28-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="aaf28-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="aaf28-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aaf28-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaf28-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aaf28-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aaf28-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aaf28-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaf28-123">Requirements</span></span>



| <span data-ttu-id="aaf28-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaf28-124">Requirement</span></span> | <span data-ttu-id="aaf28-125">Value</span><span class="sxs-lookup"><span data-stu-id="aaf28-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf28-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aaf28-126">Header</span></span><br/>  | <dl> <span data-ttu-id="aaf28-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaf28-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aaf28-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aaf28-128">Library</span></span><br/> | <dl> <span data-ttu-id="aaf28-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaf28-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf28-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaf28-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf28-131">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="aaf28-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="aaf28-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="aaf28-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




