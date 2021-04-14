---
description: Los valores del registro se deben establecer para que los verbos controlen las situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores de registro independientes para cada una de estas tres situaciones que admite el verbo.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Cómo emplear el modelo de selección de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985447"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="cb2eb-104">Cómo emplear el modelo de selección de verbos</span><span class="sxs-lookup"><span data-stu-id="cb2eb-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="cb2eb-105">Los valores del registro se deben establecer para que los verbos controlen las situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="cb2eb-106">Un verbo requiere valores de registro independientes para cada una de estas tres situaciones que admite el verbo.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="cb2eb-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="cb2eb-107">Instructions</span></span>


<span data-ttu-id="cb2eb-108">Especifique el valor de MultiSelectModel para todos los verbos.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="cb2eb-109">Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="cb2eb-110">En el caso de los métodos basados en COM (como DropTarget y ExecuteCommand), se supone que el **jugador** y para el resto **de métodos se** supone.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="cb2eb-111">Los valores posibles para el modelo de selección de verbos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cb2eb-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="cb2eb-112">Especifique **Single** para los verbos que solo admiten una sola selección.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="cb2eb-113">Especifique **Player** para los verbos que admiten cualquier número de elementos.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="cb2eb-114">Especifique el **documento** para los verbos que crean una ventana de nivel superior para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="cb2eb-115">Esto limita el número de elementos que están activados y ayuda a evitar quedarse sin recursos del sistema si el usuario abre demasiadas ventanas.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb2eb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb2eb-116">Remarks</span></span>

<span data-ttu-id="cb2eb-117">Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados que se describen en la tabla siguiente, el verbo no aparece.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="cb2eb-118">Tipo de implementación de verbo</span><span class="sxs-lookup"><span data-stu-id="cb2eb-118">Type of verb implementation</span></span> | <span data-ttu-id="cb2eb-119">Documento</span><span class="sxs-lookup"><span data-stu-id="cb2eb-119">Document</span></span> | <span data-ttu-id="cb2eb-120">Reproductor</span><span class="sxs-lookup"><span data-stu-id="cb2eb-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="cb2eb-121">Heredado</span><span class="sxs-lookup"><span data-stu-id="cb2eb-121">Legacy</span></span>                      | <span data-ttu-id="cb2eb-122">15 elementos</span><span class="sxs-lookup"><span data-stu-id="cb2eb-122">15 items</span></span> | <span data-ttu-id="cb2eb-123">100 elementos</span><span class="sxs-lookup"><span data-stu-id="cb2eb-123">100 items</span></span> |
| <span data-ttu-id="cb2eb-124">COM</span><span class="sxs-lookup"><span data-stu-id="cb2eb-124">COM</span></span>                         | <span data-ttu-id="cb2eb-125">15 elementos</span><span class="sxs-lookup"><span data-stu-id="cb2eb-125">15 items</span></span> | <span data-ttu-id="cb2eb-126">Sin límite</span><span class="sxs-lookup"><span data-stu-id="cb2eb-126">No limit</span></span>  |



 

<span data-ttu-id="cb2eb-127">A continuación se muestran las entradas del registro de ejemplo que usan el valor MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="cb2eb-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



