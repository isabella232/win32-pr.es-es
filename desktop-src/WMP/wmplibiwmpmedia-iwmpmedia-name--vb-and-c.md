---
title: Propiedad nombre de IWMPMedia
description: La propiedad Name obtiene o establece el nombre del elemento multimedia.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- propiedad nombre Media Player Windows
- propiedad nombre Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad Name
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671571"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="24df7-106">IWMPMedia:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="24df7-106">IWMPMedia::name property</span></span>

<span data-ttu-id="24df7-107">La propiedad **Name** obtiene o establece el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="24df7-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="24df7-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="24df7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="24df7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24df7-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="24df7-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="24df7-110">Property value</span></span>

<span data-ttu-id="24df7-111">**System. String** que es el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="24df7-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="24df7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24df7-112">Remarks</span></span>

<span data-ttu-id="24df7-113">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="24df7-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="24df7-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="24df7-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="24df7-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="24df7-115">Examples</span></span>

<span data-ttu-id="24df7-116">En el ejemplo siguiente se usa **Name** para cambiar el nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="24df7-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="24df7-117">Un cuadro de texto permite al usuario escribir un nuevo nombre y el nombre se cambia en respuesta al evento de clic de un botón.</span><span class="sxs-lookup"><span data-stu-id="24df7-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="24df7-118">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="24df7-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="24df7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24df7-119">Requirements</span></span>



| <span data-ttu-id="24df7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="24df7-120">Requirement</span></span> | <span data-ttu-id="24df7-121">Value</span><span class="sxs-lookup"><span data-stu-id="24df7-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24df7-122">Versión</span><span class="sxs-lookup"><span data-stu-id="24df7-122">Version</span></span><br/>   | <span data-ttu-id="24df7-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="24df7-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="24df7-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24df7-124">Namespace</span></span><br/> | <span data-ttu-id="24df7-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="24df7-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="24df7-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="24df7-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="24df7-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="24df7-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24df7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="24df7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24df7-129">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="24df7-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





