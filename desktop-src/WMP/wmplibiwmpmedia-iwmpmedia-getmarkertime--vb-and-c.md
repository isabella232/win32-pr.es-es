---
title: IWMPMedia getMarkerTime, método
description: El método getMarkerTime devuelve la hora del marcador en el índice especificado.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- método getMarkerTime de Windows Media Player
- método getMarkerTime Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getMarkerTime
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df171977adeee3b597cab1f40469af1d975425c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671577"
---
# <a name="iwmpmediagetmarkertime-method"></a><span data-ttu-id="88634-106">IWMPMedia:: getMarkerTime (método)</span><span class="sxs-lookup"><span data-stu-id="88634-106">IWMPMedia::getMarkerTime method</span></span>

<span data-ttu-id="88634-107">El método **getMarkerTime** devuelve la hora del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="88634-107">The **getMarkerTime** method returns the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="88634-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88634-108">Syntax</span></span>


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a><span data-ttu-id="88634-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88634-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88634-110">*MarkerNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88634-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88634-111">**System. Int32** que es el índice del marcador.</span><span class="sxs-lookup"><span data-stu-id="88634-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88634-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88634-112">Return value</span></span>

<span data-ttu-id="88634-113">**System. Double** que es la hora del marcador.</span><span class="sxs-lookup"><span data-stu-id="88634-113">A **System.Double** that is the marker time.</span></span>

## <a name="remarks"></a><span data-ttu-id="88634-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88634-114">Remarks</span></span>

<span data-ttu-id="88634-115">Este método devuelve **null** si el marcador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="88634-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="88634-116">Algunos elementos multimedia no contienen marcadores.</span><span class="sxs-lookup"><span data-stu-id="88634-116">Some media items do not contain markers.</span></span> <span data-ttu-id="88634-117">Use **markerCount** para averiguar el número de marcadores que hay en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="88634-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="88634-118">Los números de índice de marcador empiezan en 1.</span><span class="sxs-lookup"><span data-stu-id="88634-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="88634-119">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88634-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="88634-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="88634-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88634-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88634-121">Examples</span></span>

<span data-ttu-id="88634-122">En el ejemplo de código siguiente se usa **getMarkerTime** para rellenar un cuadro de texto de varias líneas con la ubicación de cada marcador.</span><span class="sxs-lookup"><span data-stu-id="88634-122">The following code example uses **getMarkerTime** to fill a multi-line text box with the location of each marker.</span></span> <span data-ttu-id="88634-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="88634-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a><span data-ttu-id="88634-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88634-124">Requirements</span></span>



| <span data-ttu-id="88634-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="88634-125">Requirement</span></span> | <span data-ttu-id="88634-126">Value</span><span class="sxs-lookup"><span data-stu-id="88634-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88634-127">Versión</span><span class="sxs-lookup"><span data-stu-id="88634-127">Version</span></span><br/>   | <span data-ttu-id="88634-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="88634-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="88634-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88634-129">Namespace</span></span><br/> | <span data-ttu-id="88634-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="88634-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="88634-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="88634-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="88634-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="88634-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88634-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="88634-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88634-134">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="88634-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="88634-135">**IWMPMedia. markerCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="88634-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





