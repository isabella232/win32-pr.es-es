---
description: Un mapa de valores es una matriz vinculada a una propiedad con los calificadores Value y ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Valores de ValueMap y calificadores de valor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706745"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="073db-103">Valores de ValueMap y calificadores de valor</span><span class="sxs-lookup"><span data-stu-id="073db-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="073db-104">Un mapa de valores es una matriz vinculada a una propiedad con los calificadores **Value** y **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="073db-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="073db-105">La propiedad actúa como un índice en la matriz y contiene un valor que representa uno de los valores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="073db-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="073db-106">Con el código MOF, puede tener los siguientes tipos de asignaciones de valores:</span><span class="sxs-lookup"><span data-stu-id="073db-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="073db-107">Asignación de matriz a un entero.</span><span class="sxs-lookup"><span data-stu-id="073db-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="073db-108">Puede definir una matriz con el calificador de **valor** y vincular la matriz directamente a una propiedad de entero, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="073db-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="073db-109">En este ejemplo, el valor de la propiedad **status** es un índice de la matriz de cadenas definida por **Value**.</span><span class="sxs-lookup"><span data-stu-id="073db-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="073db-110">La propiedad solo puede tomar valores que correspondan a las posiciones ordinales de la matriz de **valores** menos 1.</span><span class="sxs-lookup"><span data-stu-id="073db-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="073db-111">Por ejemplo, establecer el **Estado** en "1" se asigna al valor "error".</span><span class="sxs-lookup"><span data-stu-id="073db-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="073db-112">La propiedad de índice solo puede aceptar valores que correspondan a posiciones de la matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="073db-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="073db-113">Por ejemplo, si la matriz tiene 10 entradas, la propiedad de índice puede tener la historia 0 a 9, no 30 o 177.</span><span class="sxs-lookup"><span data-stu-id="073db-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="073db-114">Asignación de matriz a otra matriz asignada a un entero.</span><span class="sxs-lookup"><span data-stu-id="073db-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="073db-115">Si desea crear un índice que no use un sistema ordinal de recuento, use el calificador **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="073db-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="073db-116">El calificador **ValueMap** configura otra matriz que contiene un sistema de numeración de índices arbitrario, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="073db-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="073db-117">Aunque debe colocar los valores de **ValueMap** entre comillas, WMI tiene en cuenta los valores enteros.</span><span class="sxs-lookup"><span data-stu-id="073db-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="073db-118">Por lo tanto, en este ejemplo, puede establecer la propiedad **status** en un entero en **ValueMap** set: 1, 3, 99 o 0.</span><span class="sxs-lookup"><span data-stu-id="073db-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="073db-119">WMI asigna cada entero de una posición ordinal de la matriz de cadenas **ValueMap** a la posición correspondiente en la matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="073db-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="073db-120">Por ejemplo, establecer el **Estado** en 0 se asigna a "Unknown".</span><span class="sxs-lookup"><span data-stu-id="073db-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="073db-121">Asignación de matriz a otra matriz asignada a una cadena.</span><span class="sxs-lookup"><span data-stu-id="073db-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="073db-122">Si no desea utilizar un entero para indizar la matriz, en su lugar puede usar una cadena que contenga uno de los valores posibles de la matriz.</span><span class="sxs-lookup"><span data-stu-id="073db-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="073db-123">Para ello, debe definir una matriz de **valores** y **ValueMap** que contengan cadenas, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="073db-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="073db-124">Con una propiedad de cadena, los valores reales permitidos de la propiedad son las entradas de la matriz **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="073db-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="073db-125">Por ejemplo, puede establecer el **Estado** en "correcto" o "desconocido".</span><span class="sxs-lookup"><span data-stu-id="073db-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="073db-126">Depende de la aplicación aprovechar las asignaciones de una manera útil.</span><span class="sxs-lookup"><span data-stu-id="073db-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="073db-127">Depende del proveedor aplicar un intervalo de valores válido.</span><span class="sxs-lookup"><span data-stu-id="073db-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="073db-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="073db-128">Remarks</span></span>

<span data-ttu-id="073db-129">A **la hora** de decidir si usar los / calificadores de **valor**  / de **BitValues** o de mapa de bits, determine si alguno de los valores que se indican podría producirse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="073db-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="073db-130">Si pueden existir varios valores simultáneos, debe usar el **mapa de bits** / **BitValues**.</span><span class="sxs-lookup"><span data-stu-id="073db-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="073db-131">Si todos los valores son mutuamente excluyentes, debe usar los  / calificadores de **valor** de ValueMap.</span><span class="sxs-lookup"><span data-stu-id="073db-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="073db-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="073db-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="073db-133">Mapa de bits y BitValues</span><span class="sxs-lookup"><span data-stu-id="073db-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



