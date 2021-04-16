---
title: THEME. currentViewID
description: El atributo currentViewID especifica o recupera la vista mostrada actualmente.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- Media Player de Windows de THEME. currentViewID
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649855"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="51bde-104">THEME. currentViewID</span><span class="sxs-lookup"><span data-stu-id="51bde-104">THEME.currentViewID</span></span>

<span data-ttu-id="51bde-105">El atributo **currentViewID** especifica o recupera la **vista** mostrada actualmente.</span><span class="sxs-lookup"><span data-stu-id="51bde-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="51bde-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="51bde-106">Possible Values</span></span>

<span data-ttu-id="51bde-107">Este atributo es una **cadena** de lectura/escritura que especifica el **identificador** de la **vista** actual.</span><span class="sxs-lookup"><span data-stu-id="51bde-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="51bde-108">No tiene valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="51bde-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51bde-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51bde-109">Remarks</span></span>

<span data-ttu-id="51bde-110">Al especificar **currentViewID** se cierra automáticamente el **currentView** existente (al que apunta el atributo global de **vista** ) y se abre la **vista** especificada.</span><span class="sxs-lookup"><span data-stu-id="51bde-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="51bde-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51bde-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="51bde-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51bde-112">Requirements</span></span>



| <span data-ttu-id="51bde-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="51bde-113">Requirement</span></span> | <span data-ttu-id="51bde-114">Value</span><span class="sxs-lookup"><span data-stu-id="51bde-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="51bde-115">Versión</span><span class="sxs-lookup"><span data-stu-id="51bde-115">Version</span></span><br/> | <span data-ttu-id="51bde-116">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="51bde-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51bde-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="51bde-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bde-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="51bde-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





