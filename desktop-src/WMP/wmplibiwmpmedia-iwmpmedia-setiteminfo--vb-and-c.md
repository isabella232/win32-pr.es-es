---
title: IWMPMedia setItemInfo, método
description: El método setItemInfo establece el valor del atributo especificado para el elemento multimedia.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670916"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="3045c-106">IWMPMedia:: setItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="3045c-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="3045c-107">El método **setItemInfo** establece el valor del atributo especificado para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="3045c-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="3045c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3045c-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="3045c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3045c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3045c-110">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3045c-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3045c-111">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="3045c-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="3045c-112">*bstrVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3045c-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3045c-113">**System. String** que es el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="3045c-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3045c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3045c-114">Return value</span></span>

<span data-ttu-id="3045c-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3045c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3045c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3045c-116">Remarks</span></span>

<span data-ttu-id="3045c-117">La propiedad **attributeCount** obtiene el número de atributos disponibles para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="3045c-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="3045c-118">Los números de índice se pueden usar con el método **getAttributeName** para determinar los nombres de los atributos integrados que se pueden usar con este método.</span><span class="sxs-lookup"><span data-stu-id="3045c-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="3045c-119">Antes de usar este método, utilice el método **isReadOnlyItem** para detectar si un atributo determinado se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="3045c-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="3045c-120">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3045c-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="3045c-121">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3045c-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3045c-122">Nota</span><span class="sxs-lookup"><span data-stu-id="3045c-122">Note</span></span>

<span data-ttu-id="3045c-123">Si incrusta el control Media Player de Windows en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="3045c-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="3045c-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3045c-124">Examples</span></span>

<span data-ttu-id="3045c-125">En el ejemplo siguiente se usa **setItemInfo** para cambiar el valor del atributo Genre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="3045c-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="3045c-126">Un cuadro de texto permite al usuario escribir una cadena, que se utiliza para cambiar la información del atributo en respuesta al evento de clic de un botón.</span><span class="sxs-lookup"><span data-stu-id="3045c-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="3045c-127">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="3045c-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3045c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3045c-128">Requirements</span></span>



| <span data-ttu-id="3045c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3045c-129">Requirement</span></span> | <span data-ttu-id="3045c-130">Value</span><span class="sxs-lookup"><span data-stu-id="3045c-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3045c-131">Versión</span><span class="sxs-lookup"><span data-stu-id="3045c-131">Version</span></span><br/>   | <span data-ttu-id="3045c-132">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3045c-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3045c-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3045c-133">Namespace</span></span><br/> | <span data-ttu-id="3045c-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3045c-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3045c-135">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3045c-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3045c-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3045c-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3045c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3045c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3045c-138">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3045c-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3045c-139">**IWMPMedia. attributeCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3045c-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3045c-140">**IWMPMedia. getAttributeName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3045c-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3045c-141">**IWMPMedia. isReadOnlyItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3045c-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





