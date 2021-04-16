---
title: StringCollection. getItemInfo (método)
description: El método getItemInfo recupera la cadena correspondiente al índice y el nombre del elemento StringCollection especificado.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718788"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="afff2-106">StringCollection. getItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="afff2-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="afff2-107">El método **getItemInfo** recupera la cadena correspondiente al índice y el nombre del elemento **StringCollection** especificado.</span><span class="sxs-lookup"><span data-stu-id="afff2-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="afff2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afff2-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="afff2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afff2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afff2-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="afff2-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afff2-111">**Número** (**Long**) que especifica el índice de base cero del elemento **StringCollection** del que se va a obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="afff2-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="afff2-112">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="afff2-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afff2-113">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="afff2-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afff2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afff2-114">Return value</span></span>

<span data-ttu-id="afff2-115">Este método devuelve una **cadena** que representa el valor del atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="afff2-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="afff2-116">En el caso de los atributos cuyo valor subyacente es **booleano**, devuelve la cadena "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="afff2-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="afff2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afff2-117">Remarks</span></span>

<span data-ttu-id="afff2-118">Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="afff2-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="afff2-119">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="afff2-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="afff2-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="afff2-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afff2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afff2-121">Requirements</span></span>



| <span data-ttu-id="afff2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="afff2-122">Requirement</span></span> | <span data-ttu-id="afff2-123">Value</span><span class="sxs-lookup"><span data-stu-id="afff2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afff2-124">Versión</span><span class="sxs-lookup"><span data-stu-id="afff2-124">Version</span></span><br/> | <span data-ttu-id="afff2-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="afff2-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="afff2-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="afff2-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="afff2-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afff2-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afff2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="afff2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afff2-129">**StringCollection. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="afff2-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="afff2-130">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="afff2-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





