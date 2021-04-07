---
description: 'Más información acerca de: estructura de JET_TUPLELIMITS'
title: Estructura de JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003077"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="8c588-103">Estructura de JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="8c588-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="8c588-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c588-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="8c588-105">Estructura de JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="8c588-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="8c588-106">La estructura de **JET_TUPLELIMITS** permite la personalización de las características del índice de tupla por índice, en lugar de por instancia, mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="8c588-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="8c588-107">**Windows Server 2003:** La estructura de **JET_TUPLELIMITS** se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c588-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="8c588-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c588-108">Members</span></span>

<span data-ttu-id="8c588-109">**chLengthMin**</span><span class="sxs-lookup"><span data-stu-id="8c588-109">**chLengthMin**</span></span>

<span data-ttu-id="8c588-110">Longitud mínima de una tupla.</span><span class="sxs-lookup"><span data-stu-id="8c588-110">The minimum length of a tuple.</span></span> <span data-ttu-id="8c588-111">El valor predeterminado es 3.</span><span class="sxs-lookup"><span data-stu-id="8c588-111">The default value is 3.</span></span>

<span data-ttu-id="8c588-112">**chLengthMax**</span><span class="sxs-lookup"><span data-stu-id="8c588-112">**chLengthMax**</span></span>

<span data-ttu-id="8c588-113">Longitud máxima de una tupla.</span><span class="sxs-lookup"><span data-stu-id="8c588-113">The maximum length of a tuple.</span></span> <span data-ttu-id="8c588-114">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="8c588-114">The default value is 10.</span></span>

<span data-ttu-id="8c588-115">**chToIndexMax**</span><span class="sxs-lookup"><span data-stu-id="8c588-115">**chToIndexMax**</span></span>

<span data-ttu-id="8c588-116">Longitud máxima de una cadena que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="8c588-116">The maximum length of a string to index.</span></span> <span data-ttu-id="8c588-117">Por ejemplo, si una columna tiene una longitud de 100 caracteres y **chToIndexMax** está establecido en 60, solo se indexarán los primeros 60 caracteres de la columna.</span><span class="sxs-lookup"><span data-stu-id="8c588-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="8c588-118">El valor predeterminado es 32767.</span><span class="sxs-lookup"><span data-stu-id="8c588-118">The default value is 32767.</span></span>

<span data-ttu-id="8c588-119">**cchIncrement**</span><span class="sxs-lookup"><span data-stu-id="8c588-119">**cchIncrement**</span></span>

<span data-ttu-id="8c588-120">Esto permite configurar el intervalo por índice.</span><span class="sxs-lookup"><span data-stu-id="8c588-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="8c588-121">**Windows Vista:** El miembro **cchIncrement** se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c588-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="8c588-122">Antes de Windows Vista, la cantidad de desplazamiento de la ventana (el "intervalo") era siempre 1, como se muestra en el ejemplo de la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8c588-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="8c588-123">**ichStart**</span><span class="sxs-lookup"><span data-stu-id="8c588-123">**ichStart**</span></span>

<span data-ttu-id="8c588-124">Desplazamiento en el valor que se va a comenzar a recuperar las tuplas del valor.</span><span class="sxs-lookup"><span data-stu-id="8c588-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="8c588-125">**Windows Vista:** El miembro **ichStart** se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c588-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="8c588-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c588-126">Remarks</span></span>

<span data-ttu-id="8c588-127">Un índice de tupla recorre una cadena y indexa todas sus subcadenas posibles de **chLengthMax**.</span><span class="sxs-lookup"><span data-stu-id="8c588-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="8c588-128">Al final de la cadena (o en la posición **chToIndexMax**, lo que ocurra primero), se indizarán las subcadenas de al menos **chLengthMin** .</span><span class="sxs-lookup"><span data-stu-id="8c588-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="8c588-129">Un índice de tupla se puede usar para buscar cadenas con caracteres comodín iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="8c588-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="8c588-130">Suponiendo que una fila tiene un campo de texto de "RAIN IN España \! ", si se crea un índice de tupla con los parámetros **chLengthMin**= 2 y **chLengthMax**= 3, se crean las siguientes entradas en el índice:</span><span class="sxs-lookup"><span data-stu-id="8c588-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="8c588-131">Rai</span><span class="sxs-lookup"><span data-stu-id="8c588-131">"RAI"</span></span>  
<span data-ttu-id="8c588-132">UN valoren</span><span class="sxs-lookup"><span data-stu-id="8c588-132">"AIN"</span></span>  
<span data-ttu-id="8c588-133">DE</span><span class="sxs-lookup"><span data-stu-id="8c588-133">"IN "</span></span>  
<span data-ttu-id="8c588-134">"N I"</span><span class="sxs-lookup"><span data-stu-id="8c588-134">"N I"</span></span>  
<span data-ttu-id="8c588-135">DE</span><span class="sxs-lookup"><span data-stu-id="8c588-135">" IN"</span></span>  
<span data-ttu-id="8c588-136">DE</span><span class="sxs-lookup"><span data-stu-id="8c588-136">"IN "</span></span>  
<span data-ttu-id="8c588-137">"N S"</span><span class="sxs-lookup"><span data-stu-id="8c588-137">"N S"</span></span>  
<span data-ttu-id="8c588-138">DAÑADO</span><span class="sxs-lookup"><span data-stu-id="8c588-138">" SP"</span></span>  
<span data-ttu-id="8c588-139">Spa</span><span class="sxs-lookup"><span data-stu-id="8c588-139">"SPA"</span></span>  
<span data-ttu-id="8c588-140">"PAI"</span><span class="sxs-lookup"><span data-stu-id="8c588-140">"PAI"</span></span>  
<span data-ttu-id="8c588-141">UN valoren</span><span class="sxs-lookup"><span data-stu-id="8c588-141">"AIN"</span></span>  
<span data-ttu-id="8c588-142">"IN \! "</span><span class="sxs-lookup"><span data-stu-id="8c588-142">"IN\!"</span></span>  
<span data-ttu-id="8c588-143">"N \! "</span><span class="sxs-lookup"><span data-stu-id="8c588-143">"N\!"</span></span>

<span data-ttu-id="8c588-144">Tenga en cuenta que "IN" se produce dos veces y que la última entrada ("N \! ") es más corta que 3 (**chLengthMax**).</span><span class="sxs-lookup"><span data-stu-id="8c588-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="8c588-145">Tenga en cuenta también que el algoritmo de división no es compatible con espacios ni palabras, y trata todos los caracteres de forma idéntica.</span><span class="sxs-lookup"><span data-stu-id="8c588-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="8c588-146">**Windows XP:** Windows XP admite índices de tupla, pero no tiene **JET_TUPLELIMITS**.</span><span class="sxs-lookup"><span data-stu-id="8c588-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="8c588-147">El motor de base de datos usará los valores predeterminados (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767).</span><span class="sxs-lookup"><span data-stu-id="8c588-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="8c588-148">Todavía es posible cambiar estos valores, pero se establecen en función de cada instancia mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)y [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8c588-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="8c588-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c588-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c588-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8c588-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c588-151">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c588-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c588-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8c588-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c588-153">Requiere Windows Server 2008, Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c588-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c588-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8c588-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c588-155">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8c588-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8c588-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c588-156">See Also</span></span>

[<span data-ttu-id="8c588-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="8c588-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="8c588-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8c588-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="8c588-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="8c588-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="8c588-160">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="8c588-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
