---
title: IWMPQuery beginNextGroup, método
description: El método beginNextGroup comienza un nuevo grupo de condiciones. | IWMPQuery beginNextGroup, método
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- método beginNextGroup de Windows Media Player
- método beginNextGroup Windows Media Player, interfaz IWMPQuery
- Interfaz IWMPQuery Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718881"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="3c783-107">IWMPQuery:: beginNextGroup (método)</span><span class="sxs-lookup"><span data-stu-id="3c783-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="3c783-108">El método **beginNextGroup** comienza un nuevo grupo de condiciones.</span><span class="sxs-lookup"><span data-stu-id="3c783-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c783-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c783-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="3c783-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c783-110">Parameters</span></span>

<span data-ttu-id="3c783-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3c783-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c783-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c783-112">Return value</span></span>

<span data-ttu-id="3c783-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3c783-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c783-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c783-114">Remarks</span></span>

<span data-ttu-id="3c783-115">El inicio de un nuevo grupo de condiciones implica que se ha completado el grupo de condiciones actual.</span><span class="sxs-lookup"><span data-stu-id="3c783-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="3c783-116">El nuevo grupo de condiciones siempre se concatena al grupo de condiciones anterior mediante la lógica **o** .</span><span class="sxs-lookup"><span data-stu-id="3c783-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="3c783-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c783-117">Examples</span></span>

<span data-ttu-id="3c783-118">En el ejemplo siguiente se crea una consulta compleja mediante la combinación de dos grupos, cada uno de los cuales contiene una condición.</span><span class="sxs-lookup"><span data-stu-id="3c783-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="3c783-119">Los resultados de la consulta se extraen como una colección de cadenas y se muestran en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="3c783-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="3c783-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="3c783-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="3c783-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c783-121">Requirements</span></span>



| <span data-ttu-id="3c783-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c783-122">Requirement</span></span> | <span data-ttu-id="3c783-123">Value</span><span class="sxs-lookup"><span data-stu-id="3c783-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c783-124">Versión</span><span class="sxs-lookup"><span data-stu-id="3c783-124">Version</span></span><br/>   | <span data-ttu-id="3c783-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3c783-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="3c783-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c783-126">Namespace</span></span><br/> | <span data-ttu-id="3c783-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3c783-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3c783-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3c783-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3c783-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3c783-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c783-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c783-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c783-131">**IWMPMediaCollection2. createQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c783-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c783-132">**IWMPMediaCollection2. getPlaylistByQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c783-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c783-133">**IWMPMediaCollection2. getStringCollectionByQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c783-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c783-134">**Interfaz IWMPQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c783-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





