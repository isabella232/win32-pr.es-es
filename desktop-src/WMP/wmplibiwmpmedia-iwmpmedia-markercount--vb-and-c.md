---
title: Propiedad markerCount de IWMPMedia
description: La propiedad markerCount obtiene el número de marcadores en el elemento multimedia.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- propiedades de markerCount Media Player de Windows
- propiedad markerCount de Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671572"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="da792-106">IWMPMedia:: markerCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="da792-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="da792-107">La propiedad **markerCount** obtiene el número de marcadores en el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="da792-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="da792-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="da792-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da792-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da792-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="da792-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="da792-110">Property value</span></span>

<span data-ttu-id="da792-111">**System. Int32** que es el recuento de marcadores.</span><span class="sxs-lookup"><span data-stu-id="da792-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="da792-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da792-112">Remarks</span></span>

<span data-ttu-id="da792-113">Esta propiedad devuelve cero si un archivo no tiene ningún marcador o si el elemento multimedia no es el mismo que el especificado en AxWindowsMediaPlayer. currentMedia.</span><span class="sxs-lookup"><span data-stu-id="da792-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="da792-114">Los números de marcador comienzan en 1.</span><span class="sxs-lookup"><span data-stu-id="da792-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="da792-115">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="da792-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="da792-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="da792-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="da792-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="da792-117">Examples</span></span>

<span data-ttu-id="da792-118">En el ejemplo siguiente se usa **markerCount** para recuperar el número de marcadores en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="da792-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="da792-119">Ese valor se usa como límite superior para una estructura de bucle, que recorre en iteración la lista de marcadores para recuperar cada nombre de marcador y mostrarlo en un cuadro de texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="da792-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="da792-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="da792-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="da792-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da792-121">Requirements</span></span>



| <span data-ttu-id="da792-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="da792-122">Requirement</span></span> | <span data-ttu-id="da792-123">Value</span><span class="sxs-lookup"><span data-stu-id="da792-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da792-124">Versión</span><span class="sxs-lookup"><span data-stu-id="da792-124">Version</span></span><br/>   | <span data-ttu-id="da792-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="da792-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="da792-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da792-126">Namespace</span></span><br/> | <span data-ttu-id="da792-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="da792-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="da792-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="da792-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da792-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="da792-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da792-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="da792-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da792-131">**AxWindowsMediaPlayer. currentMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="da792-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da792-132">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="da792-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





