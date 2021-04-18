---
title: THEME. closeView
description: El método closeView cierra una vista abierta.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Media Player de Windows de THEME. closeView
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649738"
---
# <a name="themecloseview"></a><span data-ttu-id="002d5-104">THEME. closeView</span><span class="sxs-lookup"><span data-stu-id="002d5-104">THEME.closeView</span></span>

<span data-ttu-id="002d5-105">El método **closeView** cierra una **vista** abierta.</span><span class="sxs-lookup"><span data-stu-id="002d5-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="002d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="002d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002d5-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*Vista*</span><span class="sxs-lookup"><span data-stu-id="002d5-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="002d5-108">**Cadena** que especifica el **identificador** de la **vista** que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="002d5-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002d5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="002d5-109">Return Value</span></span>

<span data-ttu-id="002d5-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="002d5-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="002d5-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="002d5-111">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="002d5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="002d5-112">Requirements</span></span>



| <span data-ttu-id="002d5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="002d5-113">Requirement</span></span> | <span data-ttu-id="002d5-114">Value</span><span class="sxs-lookup"><span data-stu-id="002d5-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="002d5-115">Versión</span><span class="sxs-lookup"><span data-stu-id="002d5-115">Version</span></span><br/> | <span data-ttu-id="002d5-116">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="002d5-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="002d5-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="002d5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002d5-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="002d5-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="002d5-119">**THEME. openView**</span><span class="sxs-lookup"><span data-stu-id="002d5-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





