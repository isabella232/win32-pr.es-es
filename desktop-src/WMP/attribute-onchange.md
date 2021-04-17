---
title: attribute_onchange
description: Cuando un atributo de máscara cambia de valor, se produce un evento que se puede controlar mediante un controlador de eventos. El nombre del controlador de eventos es el nombre del atributo seguido por un carácter de subrayado y \ 0034; onchange \ 0034;, como \ 0034; valor \_ onchange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699976"
---
# <a name="attribute_onchange"></a><span data-ttu-id="59366-105">atributo \_ onchange</span><span class="sxs-lookup"><span data-stu-id="59366-105">attribute\_onchange</span></span>

<span data-ttu-id="59366-106">Cuando un atributo de máscara cambia de valor, se produce un evento que se puede controlar mediante un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="59366-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="59366-107">El nombre del controlador de eventos es el nombre del atributo seguido por un carácter de subrayado y "onchange", como "valor onchange \_ ".</span><span class="sxs-lookup"><span data-stu-id="59366-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="59366-108">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="59366-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="59366-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59366-109">Requirements</span></span>



| <span data-ttu-id="59366-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="59366-110">Requirement</span></span> | <span data-ttu-id="59366-111">Value</span><span class="sxs-lookup"><span data-stu-id="59366-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="59366-112">Versión</span><span class="sxs-lookup"><span data-stu-id="59366-112">Version</span></span><br/> | <span data-ttu-id="59366-113">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="59366-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59366-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="59366-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59366-115">**Controladores de eventos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="59366-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





