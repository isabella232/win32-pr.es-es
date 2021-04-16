---
title: THEME. openView
description: El método openView abre una vista en una nueva ventana.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEME. openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680247"
---
# <a name="themeopenview"></a><span data-ttu-id="868a5-104">THEME. openView</span><span class="sxs-lookup"><span data-stu-id="868a5-104">THEME.openView</span></span>

<span data-ttu-id="868a5-105">El método **openView** abre una **vista** en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="868a5-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="868a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="868a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868a5-107"><span id="view"></span><span id="VIEW"></span>*Visores*</span><span class="sxs-lookup"><span data-stu-id="868a5-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="868a5-108">**Cadena** que especifica el **identificador** de la **vista** que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="868a5-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="868a5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="868a5-109">Return Value</span></span>

<span data-ttu-id="868a5-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="868a5-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="868a5-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="868a5-111">Examples</span></span>


```JScript
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



## <a name="requirements"></a><span data-ttu-id="868a5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="868a5-112">Requirements</span></span>



| <span data-ttu-id="868a5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="868a5-113">Requirement</span></span> | <span data-ttu-id="868a5-114">Value</span><span class="sxs-lookup"><span data-stu-id="868a5-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="868a5-115">Versión</span><span class="sxs-lookup"><span data-stu-id="868a5-115">Version</span></span><br/> | <span data-ttu-id="868a5-116">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="868a5-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="868a5-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="868a5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868a5-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="868a5-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="868a5-119">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="868a5-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="868a5-120">**THEME. openViewRelative**</span><span class="sxs-lookup"><span data-stu-id="868a5-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





