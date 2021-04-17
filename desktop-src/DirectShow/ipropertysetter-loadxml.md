---
description: El método LoadXML carga los datos de propiedad expresados en lenguaje de marcado extensible (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'IPropertySetter:: LoadXML (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679117"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="6ff99-103">IPropertySetter:: LoadXML (método)</span><span class="sxs-lookup"><span data-stu-id="6ff99-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="6ff99-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="6ff99-104">\[Deprecated.</span></span> <span data-ttu-id="6ff99-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ff99-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6ff99-106">El `LoadXML` método carga los datos de propiedad expresados en lenguaje de marcado extensible (XML).</span><span class="sxs-lookup"><span data-stu-id="6ff99-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff99-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ff99-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="6ff99-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ff99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff99-109">*PXML* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ff99-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff99-110">Puntero a la interfaz **IUnknown** de un elemento XML creado por el analizador de Microsoft XML.</span><span class="sxs-lookup"><span data-stu-id="6ff99-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff99-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ff99-111">Return value</span></span>

<span data-ttu-id="6ff99-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ff99-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6ff99-113">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6ff99-113">Possible values include the following.</span></span>



| <span data-ttu-id="6ff99-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6ff99-114">Return code</span></span>                                                                                                  | <span data-ttu-id="6ff99-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ff99-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="6ff99-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6ff99-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="6ff99-117">No hay datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ff99-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="6ff99-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6ff99-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="6ff99-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6ff99-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="6ff99-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6ff99-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="6ff99-121">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="6ff99-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="6ff99-122"><dt>**\_formato de \_ archivo no válido de VFW E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ff99-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="6ff99-123">Formato no válido.</span><span class="sxs-lookup"><span data-stu-id="6ff99-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6ff99-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ff99-124">Remarks</span></span>

<span data-ttu-id="6ff99-125">Normalmente, las aplicaciones no tendrán que usar este método.</span><span class="sxs-lookup"><span data-stu-id="6ff99-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="6ff99-126">DES lo usa internamente para cargar propiedades de archivos XTL.</span><span class="sxs-lookup"><span data-stu-id="6ff99-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="6ff99-127">Para usar este método, cree un objeto **IXMLDocument** y úselo para analizar un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="6ff99-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="6ff99-128">A continuación, use el objeto **IXMLDocument** para recuperar objetos **IXMLElement** .</span><span class="sxs-lookup"><span data-stu-id="6ff99-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="6ff99-129">Si el objeto tiene propiedades, puede pasar el puntero **IXMLElement** al método **loadXML** .</span><span class="sxs-lookup"><span data-stu-id="6ff99-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="6ff99-130">El método carga las propiedades en el establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ff99-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="6ff99-131">Las interfaces **IXMLDocument** y **IXMLElement** se implementan en Microsoft XML Core Services (MSXML) versión 1,0, pero no se implementan en versiones más recientes de MSXML.</span><span class="sxs-lookup"><span data-stu-id="6ff99-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="6ff99-132">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="6ff99-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6ff99-133">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6ff99-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6ff99-134">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6ff99-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ff99-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ff99-135">Requirements</span></span>



| <span data-ttu-id="6ff99-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff99-136">Requirement</span></span> | <span data-ttu-id="6ff99-137">Value</span><span class="sxs-lookup"><span data-stu-id="6ff99-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff99-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ff99-138">Header</span></span><br/>  | <dl> <span data-ttu-id="6ff99-139"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff99-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6ff99-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ff99-140">Library</span></span><br/> | <dl> <span data-ttu-id="6ff99-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ff99-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff99-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ff99-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff99-143">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="6ff99-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="6ff99-144">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="6ff99-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




