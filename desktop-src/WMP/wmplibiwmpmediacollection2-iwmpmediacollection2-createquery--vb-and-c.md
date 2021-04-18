---
title: IWMPMediaCollection2 createQuery (método)
description: El método createQuery devuelve una interfaz IWMPQuery que representa una nueva consulta.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- createQuery (método) de Windows Media Player
- método createQuery Windows Media Player, interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Windows Media Player, método createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700332"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="0d0f6-106">IWMPMediaCollection2:: createQuery (método)</span><span class="sxs-lookup"><span data-stu-id="0d0f6-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="0d0f6-107">El `createQuery` método devuelve una interfaz **IWMPQuery** que representa una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0f6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d0f6-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="0d0f6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d0f6-109">Parameters</span></span>

<span data-ttu-id="0d0f6-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d0f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d0f6-111">Return value</span></span>

<span data-ttu-id="0d0f6-112">Una interfaz **WMPLib. IWMPQuery** que representa una nueva consulta vacía.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0f6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d0f6-113">Remarks</span></span>

<span data-ttu-id="0d0f6-114">La creación de una nueva consulta es el primer paso para crear una consulta compuesta.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="0d0f6-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d0f6-115">Examples</span></span>

<span data-ttu-id="0d0f6-116">En el ejemplo siguiente `createQuery` se usa para obtener una interfaz **IWMPQuery** que se inicializa en NULL.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="0d0f6-117">Dado que esta consulta no tiene ninguna condición agregada, cuando se usa como argumento en el método **getStringCollectionByQuery** , el método devolverá una colección de cadenas que contiene todos los elementos multimedia del tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="0d0f6-118">A continuación, la colección de cadenas se muestra en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="0d0f6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d0f6-119">Requirements</span></span>



| <span data-ttu-id="0d0f6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d0f6-120">Requirement</span></span> | <span data-ttu-id="0d0f6-121">Value</span><span class="sxs-lookup"><span data-stu-id="0d0f6-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0f6-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0d0f6-122">Version</span></span><br/>   | <span data-ttu-id="0d0f6-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0d0f6-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d0f6-124">Namespace</span></span><br/> | <span data-ttu-id="0d0f6-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0d0f6-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="0d0f6-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0d0f6-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0d0f6-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0f6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d0f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0f6-129">**Interfaz IWMPMediaCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d0f6-130">**Interfaz IWMPQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





