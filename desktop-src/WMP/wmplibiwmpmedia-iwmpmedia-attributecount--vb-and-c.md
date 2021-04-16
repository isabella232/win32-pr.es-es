---
title: Propiedad attributeCount de IWMPMedia
description: La propiedad attributeCount obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- propiedades de attributeCount Media Player de Windows
- propiedad attributeCount de Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad attributeCount
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671592"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="887c9-106">IWMPMedia:: attributeCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="887c9-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="887c9-107">La propiedad **attributeCount** obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="887c9-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="887c9-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="887c9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="887c9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="887c9-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="887c9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="887c9-110">Property value</span></span>

<span data-ttu-id="887c9-111">**System. Int32** que es el recuento.</span><span class="sxs-lookup"><span data-stu-id="887c9-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="887c9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="887c9-112">Remarks</span></span>

<span data-ttu-id="887c9-113">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="887c9-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="887c9-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="887c9-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="887c9-115">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="887c9-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="887c9-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="887c9-116">Examples</span></span>

<span data-ttu-id="887c9-117">En el ejemplo siguiente se usa **attributeCount** para determinar el número de atributos disponibles en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="887c9-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="887c9-118">El código utiliza ese valor para mostrar una lista de nombres de atributo y valores en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="887c9-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="887c9-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="887c9-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="887c9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="887c9-120">Requirements</span></span>



| <span data-ttu-id="887c9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="887c9-121">Requirement</span></span> | <span data-ttu-id="887c9-122">Value</span><span class="sxs-lookup"><span data-stu-id="887c9-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887c9-123">Versión</span><span class="sxs-lookup"><span data-stu-id="887c9-123">Version</span></span><br/>   | <span data-ttu-id="887c9-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="887c9-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="887c9-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="887c9-125">Namespace</span></span><br/> | <span data-ttu-id="887c9-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="887c9-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="887c9-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="887c9-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="887c9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="887c9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887c9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="887c9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887c9-130">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="887c9-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





