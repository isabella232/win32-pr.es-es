---
title: IWMPMedia getAttributeName, método
description: El método getAttributeName devuelve el nombre del atributo correspondiente al índice especificado.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- método getAttributeName de Windows Media Player
- método getAttributeName Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getAttributeName
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671589"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="19264-106">IWMPMedia:: getAttributeName (método)</span><span class="sxs-lookup"><span data-stu-id="19264-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="19264-107">El método **getAttributeName** devuelve el nombre del atributo correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="19264-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="19264-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19264-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="19264-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19264-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19264-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19264-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19264-111">**System. Int32** que es el índice.</span><span class="sxs-lookup"><span data-stu-id="19264-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19264-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19264-112">Return value</span></span>

<span data-ttu-id="19264-113">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="19264-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="19264-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19264-114">Remarks</span></span>

<span data-ttu-id="19264-115">El nombre de atributo devuelto se puede usar junto con **getItemInfo** para recuperar el valor de un atributo con nombre específico.</span><span class="sxs-lookup"><span data-stu-id="19264-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="19264-116">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="19264-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="19264-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="19264-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="19264-118">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="19264-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="19264-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="19264-119">Examples</span></span>

<span data-ttu-id="19264-120">En el ejemplo siguiente se usa **getAttributeName** para rellenar un cuadro de texto de varias líneas con el índice y el nombre de cada atributo del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="19264-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="19264-121">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="19264-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="19264-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19264-122">Requirements</span></span>



| <span data-ttu-id="19264-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19264-123">Requirement</span></span> | <span data-ttu-id="19264-124">Value</span><span class="sxs-lookup"><span data-stu-id="19264-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19264-125">Versión</span><span class="sxs-lookup"><span data-stu-id="19264-125">Version</span></span><br/>   | <span data-ttu-id="19264-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="19264-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="19264-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19264-127">Namespace</span></span><br/> | <span data-ttu-id="19264-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="19264-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="19264-129">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="19264-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="19264-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="19264-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19264-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="19264-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19264-132">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19264-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19264-133">**IWMPMedia. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19264-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





