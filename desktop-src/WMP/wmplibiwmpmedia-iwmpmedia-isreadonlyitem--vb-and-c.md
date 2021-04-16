---
title: IWMPMedia isReadOnlyItem, método
description: El método isReadOnlyItem devuelve un valor que indica si se pueden editar los atributos del elemento multimedia especificado.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- método isReadOnlyItem de Windows Media Player
- método isReadOnlyItem Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método isReadOnlyItem
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671573"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="ddade-106">IWMPMedia:: isReadOnlyItem (método)</span><span class="sxs-lookup"><span data-stu-id="ddade-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="ddade-107">El método **isReadOnlyItem** devuelve un valor que indica si se pueden editar los atributos del elemento multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="ddade-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddade-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddade-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="ddade-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddade-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddade-110">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddade-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddade-111">**System. String** que es el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="ddade-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddade-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddade-112">Return value</span></span>

<span data-ttu-id="ddade-113">Valor **System. Boolean** que indica si los atributos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ddade-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddade-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddade-114">Remarks</span></span>

<span data-ttu-id="ddade-115">Si un atributo es de solo lectura, no se puede establecer con el método **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="ddade-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="ddade-116">Tenga en cuenta que este método puede devolver valores diferentes para un atributo determinado cuando se usa con versiones diferentes de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ddade-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="ddade-117">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ddade-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ddade-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ddade-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ddade-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ddade-119">Examples</span></span>

<span data-ttu-id="ddade-120">En el ejemplo siguiente se usa **isReadOnlyItem** para rellenar un cuadro de texto de varias líneas con información sobre el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="ddade-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="ddade-121">El código muestra cada atributo del elemento multimedia actual, junto con el texto que indica si el atributo es de solo lectura o de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ddade-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="ddade-122">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="ddade-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="ddade-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddade-123">Requirements</span></span>



| <span data-ttu-id="ddade-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddade-124">Requirement</span></span> | <span data-ttu-id="ddade-125">Value</span><span class="sxs-lookup"><span data-stu-id="ddade-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddade-126">Versión</span><span class="sxs-lookup"><span data-stu-id="ddade-126">Version</span></span><br/>   | <span data-ttu-id="ddade-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ddade-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ddade-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ddade-128">Namespace</span></span><br/> | <span data-ttu-id="ddade-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ddade-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ddade-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ddade-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ddade-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ddade-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddade-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddade-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddade-133">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ddade-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ddade-134">**IWMPMedia. setItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ddade-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





