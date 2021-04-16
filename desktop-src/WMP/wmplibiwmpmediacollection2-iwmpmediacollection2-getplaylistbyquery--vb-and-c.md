---
title: IWMPMediaCollection2 getPlaylistByQuery, método
description: El método getPlaylistByQuery devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia que coinciden con las condiciones de la consulta.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- método getPlaylistByQuery de Windows Media Player
- método getPlaylistByQuery Windows Media Player, interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Windows Media Player, método getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649883"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="a4f73-106">IWMPMediaCollection2:: getPlaylistByQuery (método)</span><span class="sxs-lookup"><span data-stu-id="a4f73-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="a4f73-107">El `getPlaylistByQuery` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="a4f73-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f73-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4f73-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="a4f73-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4f73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f73-110">*pQuery* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4f73-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f73-111">La interfaz **WMPLib. IWMPQuery** que representa la consulta.</span><span class="sxs-lookup"><span data-stu-id="a4f73-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="a4f73-112">*bstrMediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4f73-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f73-113">**System. String** que es el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a4f73-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="a4f73-114">Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".</span><span class="sxs-lookup"><span data-stu-id="a4f73-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="a4f73-115">*bstrSortAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4f73-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f73-116">**System. String** que es el nombre del atributo utilizado para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="a4f73-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="a4f73-117">Una cadena de longitud cero ("") significa que no se aplica ninguna ordenación.</span><span class="sxs-lookup"><span data-stu-id="a4f73-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="a4f73-118">*fSortAscending* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4f73-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f73-119">El valor **System. Boolean** que indica si la lista de reproducción se debe ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="a4f73-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f73-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4f73-120">Return value</span></span>

<span data-ttu-id="a4f73-121">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción recuperada.</span><span class="sxs-lookup"><span data-stu-id="a4f73-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f73-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4f73-122">Remarks</span></span>

<span data-ttu-id="a4f73-123">Las consultas compuestas que usan **IWMPQuery** no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a4f73-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="a4f73-124">Cuando la consulta compuesta especificada por el parámetro *pQuery* contiene una condición generada en el atributo **mediatype** , se omite esa condición.</span><span class="sxs-lookup"><span data-stu-id="a4f73-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="a4f73-125">Siempre se usa el valor del parámetro *bstrMediaType* .</span><span class="sxs-lookup"><span data-stu-id="a4f73-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="a4f73-126">Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *bstrMediaType* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a4f73-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f73-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f73-127">Requirements</span></span>



| <span data-ttu-id="a4f73-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f73-128">Requirement</span></span> | <span data-ttu-id="a4f73-129">Value</span><span class="sxs-lookup"><span data-stu-id="a4f73-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f73-130">Versión</span><span class="sxs-lookup"><span data-stu-id="a4f73-130">Version</span></span><br/>   | <span data-ttu-id="a4f73-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="a4f73-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="a4f73-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a4f73-132">Namespace</span></span><br/> | <span data-ttu-id="a4f73-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a4f73-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a4f73-134">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a4f73-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a4f73-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f73-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f73-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4f73-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f73-137">**Interfaz IWMPMediaCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4f73-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4f73-138">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4f73-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4f73-139">**Interfaz IWMPQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4f73-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4f73-140">**MediaType (atributo)**</span><span class="sxs-lookup"><span data-stu-id="a4f73-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





