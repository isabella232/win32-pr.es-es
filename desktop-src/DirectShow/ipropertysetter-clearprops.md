---
description: El método ClearProps borra todos los datos de propiedad del establecedor de propiedad. La aplicación puede establecer nuevos datos de propiedad después de llamar a esta función.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'IPropertySetter:: ClearProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679120"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="de467-104">IPropertySetter:: ClearProps (método)</span><span class="sxs-lookup"><span data-stu-id="de467-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="de467-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="de467-105">\[Deprecated.</span></span> <span data-ttu-id="de467-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de467-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="de467-107">El `ClearProps` método borra todos los datos de propiedad del establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="de467-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="de467-108">La aplicación puede establecer nuevos datos de propiedad después de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="de467-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="de467-109">La eliminación de los datos de propiedad no restaura las propiedades del objeto a sus valores originales.</span><span class="sxs-lookup"><span data-stu-id="de467-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="de467-110">Simplemente impide que DirectShow aplique otros cambios.</span><span class="sxs-lookup"><span data-stu-id="de467-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="de467-111">Los valores de propiedad se aplican en tiempo de ejecución cuando se representa el proyecto.</span><span class="sxs-lookup"><span data-stu-id="de467-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="de467-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de467-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="de467-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de467-113">Parameters</span></span>

<span data-ttu-id="de467-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="de467-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de467-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de467-115">Return value</span></span>

<span data-ttu-id="de467-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="de467-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de467-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de467-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de467-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de467-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de467-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="de467-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="de467-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="de467-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="de467-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="de467-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de467-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de467-122">Requirements</span></span>



| <span data-ttu-id="de467-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="de467-123">Requirement</span></span> | <span data-ttu-id="de467-124">Value</span><span class="sxs-lookup"><span data-stu-id="de467-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de467-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de467-125">Header</span></span><br/>  | <dl> <span data-ttu-id="de467-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="de467-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="de467-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de467-127">Library</span></span><br/> | <dl> <span data-ttu-id="de467-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de467-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de467-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="de467-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de467-130">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="de467-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="de467-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="de467-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




