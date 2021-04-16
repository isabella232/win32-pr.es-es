---
description: El método AddProp agrega una propiedad al establecedor de propiedad, con una matriz de pares de valor de tiempo que definen el valor de la propiedad en un intervalo de tiempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'IPropertySetter:: AddProp (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679121"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="7aed6-103">IPropertySetter:: AddProp (método)</span><span class="sxs-lookup"><span data-stu-id="7aed6-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="7aed6-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7aed6-104">\[Deprecated.</span></span> <span data-ttu-id="7aed6-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7aed6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7aed6-106">El `AddProp` método agrega una propiedad al establecedor de propiedad, con una matriz de pares de valor de tiempo que definen el valor de la propiedad en un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7aed6-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aed6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7aed6-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="7aed6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7aed6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aed6-109">*Parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7aed6-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aed6-110">[**Dexterity \_**](dexter-param.md) Estructura de parámetro que especifica la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7aed6-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="7aed6-111">El miembro **nvalores** de la estructura debe ser igual al tamaño de la matriz proporcionada en el parámetro *pavalue* .</span><span class="sxs-lookup"><span data-stu-id="7aed6-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7aed6-112">*Pavalue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7aed6-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aed6-113">Puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) que contienen pares de valor de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7aed6-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="7aed6-114">La matriz debe estar en orden de tiempo ascendente.</span><span class="sxs-lookup"><span data-stu-id="7aed6-114">The array must be in ascending time order.</span></span> <span data-ttu-id="7aed6-115">Las horas son relativas a la hora de inicio del efecto o de la transición.</span><span class="sxs-lookup"><span data-stu-id="7aed6-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aed6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7aed6-116">Return value</span></span>

<span data-ttu-id="7aed6-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7aed6-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7aed6-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7aed6-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aed6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7aed6-119">Remarks</span></span>

<span data-ttu-id="7aed6-120">La primera estructura de [**\_ valor de Dexterity**](dexter-value.md) debe especificar una hora de referencia de cero y una marca de interpolación (**dwInterp**) de **DEXTERF \_ salto**, o el método devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="7aed6-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="7aed6-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7aed6-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7aed6-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7aed6-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7aed6-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7aed6-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7aed6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aed6-124">Requirements</span></span>



| <span data-ttu-id="7aed6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aed6-125">Requirement</span></span> | <span data-ttu-id="7aed6-126">Value</span><span class="sxs-lookup"><span data-stu-id="7aed6-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aed6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7aed6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7aed6-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aed6-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7aed6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7aed6-129">Library</span></span><br/> | <dl> <span data-ttu-id="7aed6-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7aed6-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aed6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7aed6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aed6-132">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="7aed6-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="7aed6-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="7aed6-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




