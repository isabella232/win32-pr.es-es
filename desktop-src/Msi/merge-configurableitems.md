---
description: La propiedad ConfigurableItems de solo lectura del objeto Merge devuelve una colección de objetos ConfigurableItem, cada uno de los cuales representa una sola fila de la tabla ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configpropiedad urableItems (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679455"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="787aa-103">Merge.Configpropiedad urableItems</span><span class="sxs-lookup"><span data-stu-id="787aa-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="787aa-104">La propiedad **ConfigurableItems** de solo lectura del objeto [**Merge**](merge-object.md) devuelve una colección de objetos [**ConfigurableItem**](configurableitem-object.md) , cada uno de los cuales representa una sola fila de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="787aa-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="787aa-105">Semánticamente, cada interfaz del enumerador representa un elemento que puede ser configurado por el consumidor del módulo.</span><span class="sxs-lookup"><span data-stu-id="787aa-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="787aa-106">La colección es una colección de solo lectura e implementa las interfaces de colección estándar de solo lectura de Item (), Count () y \_ NewEnum ().</span><span class="sxs-lookup"><span data-stu-id="787aa-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="787aa-107">El enumerador **IEnumMsmConfigItems** implementa Next (), SKIP (), RESET () y Clone () con la semántica estándar.</span><span class="sxs-lookup"><span data-stu-id="787aa-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="787aa-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="787aa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="787aa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="787aa-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="787aa-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="787aa-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="787aa-111">C++</span><span class="sxs-lookup"><span data-stu-id="787aa-111">C++</span></span>

<span data-ttu-id="787aa-112">Consulte [**Get \_ ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span><span class="sxs-lookup"><span data-stu-id="787aa-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="787aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="787aa-113">Requirements</span></span>



| <span data-ttu-id="787aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="787aa-114">Requirement</span></span> | <span data-ttu-id="787aa-115">Value</span><span class="sxs-lookup"><span data-stu-id="787aa-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="787aa-116">Versión</span><span class="sxs-lookup"><span data-stu-id="787aa-116">Version</span></span><br/> | <span data-ttu-id="787aa-117">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="787aa-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="787aa-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="787aa-118">Header</span></span><br/>  | <dl> <span data-ttu-id="787aa-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="787aa-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="787aa-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="787aa-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="787aa-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="787aa-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




