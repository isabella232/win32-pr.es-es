---
title: IWMPMediaCollection2 getStringCollectionByQuery, método
description: El método getStringCollectionByQuery devuelve una interfaz IWMPStringCollection que proporciona acceso al conjunto de todos los valores de cadena para un atributo especificado que coincide con las condiciones de la consulta.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- método getStringCollectionByQuery de Windows Media Player
- método getStringCollectionByQuery Windows Media Player, interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Windows Media Player, método getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708949"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="c2287-106">IWMPMediaCollection2:: getStringCollectionByQuery (método)</span><span class="sxs-lookup"><span data-stu-id="c2287-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="c2287-107">El `getStringCollectionByQuery` método devuelve una interfaz **IWMPStringCollection** que proporciona acceso al conjunto de todos los valores de cadena para un atributo especificado que coincide con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c2287-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2287-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2287-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="c2287-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2287-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2287-110">*bstrAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2287-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2287-111">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="c2287-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="c2287-112">*pQuery* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2287-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2287-113">La interfaz **WMPLib. IWMPQuery** que es la consulta que define las condiciones que se usan para recuperar la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c2287-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="c2287-114">*bstrMediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2287-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2287-115">**System. String** que es el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c2287-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="c2287-116">Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".</span><span class="sxs-lookup"><span data-stu-id="c2287-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="c2287-117">*bstrSortAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2287-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2287-118">**System. String** que es el nombre del atributo utilizado para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="c2287-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="c2287-119">Una cadena de longitud cero ("") significa que no se aplica ninguna ordenación.</span><span class="sxs-lookup"><span data-stu-id="c2287-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="c2287-120">*fSortAscending* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2287-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2287-121">El valor **System. Boolean** que indica si el conjunto de valores de cadena se debe ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="c2287-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2287-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2287-122">Return value</span></span>

<span data-ttu-id="c2287-123">Una interfaz **WMPLib. IWMPStringCollection** para el conjunto recuperado de valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="c2287-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2287-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2287-124">Remarks</span></span>

<span data-ttu-id="c2287-125">Las consultas compuestas que usan **IWMPQuery** no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c2287-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="c2287-126">Cuando la consulta compuesta especificada por el parámetro *pQuery* contiene una condición generada en el atributo **mediatype** , se omite esa condición.</span><span class="sxs-lookup"><span data-stu-id="c2287-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="c2287-127">Siempre se usa el valor del parámetro *bstrMediaType* .</span><span class="sxs-lookup"><span data-stu-id="c2287-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="c2287-128">Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *bstrMediaType* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2287-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2287-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2287-129">Requirements</span></span>



| <span data-ttu-id="c2287-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2287-130">Requirement</span></span> | <span data-ttu-id="c2287-131">Value</span><span class="sxs-lookup"><span data-stu-id="c2287-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2287-132">Versión</span><span class="sxs-lookup"><span data-stu-id="c2287-132">Version</span></span><br/>   | <span data-ttu-id="c2287-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c2287-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="c2287-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2287-134">Namespace</span></span><br/> | <span data-ttu-id="c2287-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c2287-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c2287-136">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c2287-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c2287-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c2287-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2287-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2287-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2287-139">**Interfaz IWMPMediaCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c2287-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2287-140">**Interfaz IWMPQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c2287-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2287-141">**Interfaz IWMPStringCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c2287-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2287-142">**MediaType (atributo)**</span><span class="sxs-lookup"><span data-stu-id="c2287-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





