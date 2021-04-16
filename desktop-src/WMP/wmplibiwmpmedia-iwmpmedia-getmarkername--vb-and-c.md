---
title: IWMPMedia getMarkerName, método
description: El método getMarkerName devuelve el nombre del marcador en el índice especificado.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- método getMarkerName de Windows Media Player
- método getMarkerName Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getMarkerName
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671578"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="51f34-106">IWMPMedia:: getMarkerName (método)</span><span class="sxs-lookup"><span data-stu-id="51f34-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="51f34-107">El método **getMarkerName** devuelve el nombre del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="51f34-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f34-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51f34-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="51f34-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51f34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f34-110">*MarkerNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51f34-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51f34-111">**System. Int32** que es el índice del marcador.</span><span class="sxs-lookup"><span data-stu-id="51f34-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51f34-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51f34-112">Return value</span></span>

<span data-ttu-id="51f34-113">**System. String** que es el nombre del marcador.</span><span class="sxs-lookup"><span data-stu-id="51f34-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f34-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51f34-114">Remarks</span></span>

<span data-ttu-id="51f34-115">Este método devuelve **null** si el marcador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="51f34-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="51f34-116">Algunos elementos multimedia no contienen marcadores.</span><span class="sxs-lookup"><span data-stu-id="51f34-116">Some media items do not contain markers.</span></span> <span data-ttu-id="51f34-117">Use **markerCount** para averiguar el número de marcadores que hay en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="51f34-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="51f34-118">Los números de índice de marcador empiezan en 1.</span><span class="sxs-lookup"><span data-stu-id="51f34-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="51f34-119">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="51f34-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="51f34-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="51f34-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="51f34-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51f34-121">Examples</span></span>

<span data-ttu-id="51f34-122">En el ejemplo de código siguiente se usa **getMarkerName** para rellenar un cuadro de texto de varias líneas con los nombres de los marcadores del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="51f34-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="51f34-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="51f34-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="51f34-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f34-124">Requirements</span></span>



| <span data-ttu-id="51f34-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f34-125">Requirement</span></span> | <span data-ttu-id="51f34-126">Value</span><span class="sxs-lookup"><span data-stu-id="51f34-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f34-127">Versión</span><span class="sxs-lookup"><span data-stu-id="51f34-127">Version</span></span><br/>   | <span data-ttu-id="51f34-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="51f34-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="51f34-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51f34-129">Namespace</span></span><br/> | <span data-ttu-id="51f34-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="51f34-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="51f34-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="51f34-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="51f34-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="51f34-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f34-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="51f34-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f34-134">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="51f34-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51f34-135">**IWMPMedia. markerCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="51f34-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





