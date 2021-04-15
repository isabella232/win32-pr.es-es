---
title: IWMPStringCollection2 getItemInfo, método
description: El método getItemInfo devuelve la cadena correspondiente al índice y el nombre del elemento de colección de cadenas especificado.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709115"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="7d10a-106">IWMPStringCollection2:: getItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="7d10a-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="7d10a-107">El método **getItemInfo** devuelve la cadena correspondiente al índice y el nombre del elemento de colección de cadenas especificado.</span><span class="sxs-lookup"><span data-stu-id="7d10a-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d10a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d10a-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="7d10a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d10a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d10a-110">*lCollectionIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d10a-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d10a-111">**System. Int32** que especifica el índice de base cero del elemento de colección de cadenas del que se va a obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="7d10a-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="7d10a-112">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d10a-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d10a-113">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="7d10a-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d10a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d10a-114">Return value</span></span>

<span data-ttu-id="7d10a-115">**System. String** que es el nombre del elemento de colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="7d10a-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="7d10a-116">En el caso de los atributos cuyo valor subyacente es **System. Boolean**, devuelve la cadena "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="7d10a-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="7d10a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d10a-117">Remarks</span></span>

<span data-ttu-id="7d10a-118">Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="7d10a-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="7d10a-119">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7d10a-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7d10a-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7d10a-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d10a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d10a-121">Requirements</span></span>



| <span data-ttu-id="7d10a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d10a-122">Requirement</span></span> | <span data-ttu-id="7d10a-123">Value</span><span class="sxs-lookup"><span data-stu-id="7d10a-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d10a-124">Versión</span><span class="sxs-lookup"><span data-stu-id="7d10a-124">Version</span></span><br/>   | <span data-ttu-id="7d10a-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="7d10a-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="7d10a-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d10a-126">Namespace</span></span><br/> | <span data-ttu-id="7d10a-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7d10a-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7d10a-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="7d10a-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7d10a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7d10a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d10a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d10a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d10a-131">**Interfaz IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="7d10a-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7d10a-132">**IWMPStringCollection2. getItemInfoByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7d10a-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





