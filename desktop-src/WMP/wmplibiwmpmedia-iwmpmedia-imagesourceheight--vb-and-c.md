---
title: Propiedad imageSourceHeight de IWMPMedia
description: La propiedad imageSourceHeight obtiene el alto del elemento multimedia actual en píxeles.
ms.assetid: d60f1713-7110-4605-9009-45825c380546
keywords:
- propiedades de imageSourceHeight Media Player de Windows
- propiedad imageSourceHeight de Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad imageSourceHeight
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceHeight
- IWMPMedia.get_imageSourceHeight
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b80a702f119ba72220e5ac3ac86b524ce8c11c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671576"
---
# <a name="iwmpmediaimagesourceheight-property"></a><span data-ttu-id="b4c94-106">IWMPMedia:: imageSourceHeight (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b4c94-106">IWMPMedia::imageSourceHeight property</span></span>

<span data-ttu-id="b4c94-107">La propiedad **imageSourceHeight** obtiene el alto del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b4c94-107">The **imageSourceHeight** property gets the height of the current media item in pixels.</span></span>

<span data-ttu-id="b4c94-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b4c94-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c94-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4c94-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceHeight {get;}
```


```VB

Public ReadOnly Property imageSourceHeight As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b4c94-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4c94-110">Property value</span></span>

<span data-ttu-id="b4c94-111">**System. Int32** que es el alto del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="b4c94-111">A **System.Int32** that is the height of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c94-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4c94-112">Remarks</span></span>

<span data-ttu-id="b4c94-113">Si el elemento multimedia no es el actual, esta propiedad devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b4c94-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="b4c94-114">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b4c94-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="b4c94-115">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b4c94-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b4c94-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4c94-116">Examples</span></span>

<span data-ttu-id="b4c94-117">En el ejemplo siguiente se usa **imageSourceHeight** para mostrar el tamaño de la imagen, en píxeles, del elemento multimedia actual en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="b4c94-117">The following example uses **imageSourceHeight** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="b4c94-118">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="b4c94-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Store the height and width of the new media item.
         int height = player.currentMedia.imageSourceHeight;
         int width = player.currentMedia.imageSourceWidth;

         // Clear all the information in the text box.
         videoSize.Clear();

         // Test whether an image is visible.
         if (height != 0 && width != 0)
         {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
         }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b4c94-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4c94-119">Requirements</span></span>



| <span data-ttu-id="b4c94-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c94-120">Requirement</span></span> | <span data-ttu-id="b4c94-121">Value</span><span class="sxs-lookup"><span data-stu-id="b4c94-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c94-122">Versión</span><span class="sxs-lookup"><span data-stu-id="b4c94-122">Version</span></span><br/>   | <span data-ttu-id="b4c94-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b4c94-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b4c94-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4c94-124">Namespace</span></span><br/> | <span data-ttu-id="b4c94-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b4c94-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b4c94-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b4c94-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b4c94-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b4c94-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c94-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4c94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c94-129">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b4c94-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





