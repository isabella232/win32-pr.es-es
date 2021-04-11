---
description: La estructura SET define un conjunto de valores.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: ESTABLECER estructura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276835"
---
# <a name="set-structure"></a><span data-ttu-id="701d1-103">ESTABLECER estructura</span><span class="sxs-lookup"><span data-stu-id="701d1-103">SET structure</span></span>

<span data-ttu-id="701d1-104">La estructura **set** define un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="701d1-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="701d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="701d1-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="701d1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="701d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="701d1-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="701d1-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-108">Número total de entradas de un conjunto.</span><span class="sxs-lookup"><span data-stu-id="701d1-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-109">**lpByteTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-110">Puntero a una matriz de valores de BYTE.</span><span class="sxs-lookup"><span data-stu-id="701d1-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-111">**lpWordTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-112">Puntero a una matriz de valores de WORD.</span><span class="sxs-lookup"><span data-stu-id="701d1-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-113">**lpDwordTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-114">Puntero a una matriz de valores DWORD.</span><span class="sxs-lookup"><span data-stu-id="701d1-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-115">**lpLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-116">Puntero a una matriz de estructuras [LARGEINT](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="701d1-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-117">**lpSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-118">Puntero a una matriz de valores SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="701d1-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-119">**lpLabeledByteTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-120">Puntero a una matriz de estructuras de [ \_ bytes etiquetadas](labeled-byte.md) .</span><span class="sxs-lookup"><span data-stu-id="701d1-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="701d1-121">Cada estructura de **\_ bytes con etiqueta** define un valor y una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="701d1-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="701d1-122">Monitor de red muestra una etiqueta si encuentra un valor correspondiente en el paquete del protocolo.</span><span class="sxs-lookup"><span data-stu-id="701d1-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-123">**lpLabeledWordTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-124">Puntero a una matriz de estructuras de [ \_ palabras etiquetadas](labeled-word.md) que definen un conjunto de valores y etiquetas de palabra.</span><span class="sxs-lookup"><span data-stu-id="701d1-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-125">**lpLabeledDwordTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-126">Puntero a una matriz de estructuras [ \_ DWORD con etiqueta](labeled-dword.md) que definen un conjunto de valores DWORD y etiquetas.</span><span class="sxs-lookup"><span data-stu-id="701d1-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-127">**lpLabeledLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-128">Puntero a una matriz de estructuras [ \_ LARGEINT con etiqueta](labeled-largeint.md) que definen un conjunto de valores y etiquetas LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="701d1-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-129">**lpLabeledSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-130">Puntero a una matriz de estructuras [ \_ SYSTEMTIME etiquetadas](labeled-systemtime.md) que definen un conjunto de valores del sistema y etiquetas.</span><span class="sxs-lookup"><span data-stu-id="701d1-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-131">**lpLabeledBit**</span><span class="sxs-lookup"><span data-stu-id="701d1-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-132">Puntero a una matriz de estructuras de [ \_ bits con etiqueta](labeled-bit.md) que definen un conjunto de pares de bits con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="701d1-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="701d1-133">Cada BIT puede especificar dos etiquetas para cada Estado (0 o 1) del BIT.</span><span class="sxs-lookup"><span data-stu-id="701d1-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="701d1-134">**lpVoidTable**</span><span class="sxs-lookup"><span data-stu-id="701d1-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="701d1-135">Puntero a una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="701d1-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="701d1-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="701d1-136">Remarks</span></span>

<span data-ttu-id="701d1-137">La estructura **set** se usa para definir un conjunto de datos de comparación que monitor de red pueden utilizar para interpretar el valor de una propiedad en un paquete de protocolo.</span><span class="sxs-lookup"><span data-stu-id="701d1-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="701d1-138">Cuando se requiere un conjunto de datos de comparación, se especifica un puntero a la estructura de **conjunto** en el miembro **lpSet** de la estructura [PROPERTYINFO](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="701d1-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="701d1-139">El archivo DLL del analizador puede proporcionar un conjunto de valores y un conjunto de etiquetas.</span><span class="sxs-lookup"><span data-stu-id="701d1-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="701d1-140">El miembro de la **Unión** que selecciona en una estructura de **conjunto** apunta a una matriz de estructuras que definen cada miembro de un conjunto.</span><span class="sxs-lookup"><span data-stu-id="701d1-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="701d1-141">Conjunto de valores</span><span class="sxs-lookup"><span data-stu-id="701d1-141">Value set</span></span>

    <span data-ttu-id="701d1-142">Se utiliza un conjunto de valores cuando se desea que Monitor de red incluya un indicador in-set o Not-in-set con el valor que se encuentra en el paquete del protocolo.</span><span class="sxs-lookup"><span data-stu-id="701d1-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="701d1-143">Por ejemplo, si se especifica un conjunto DWORD, Monitor de red muestra una etiqueta para cada valor DWORD que se encuentra en el paquete de protocolo, lo que indica que la DWORD es o no se especifica en el conjunto.</span><span class="sxs-lookup"><span data-stu-id="701d1-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="701d1-144">Un conjunto de valores puede basarse en los tipos de datos BYTE, WORD, DWORD, LARGEINT y SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="701d1-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="701d1-145">Conjunto de etiquetas</span><span class="sxs-lookup"><span data-stu-id="701d1-145">Label set</span></span>

    <span data-ttu-id="701d1-146">Se utiliza un conjunto de etiquetas cuando se desea Monitor de red mostrar una etiqueta definida por el usuario en lugar de los valores de propiedad especificados en un conjunto.</span><span class="sxs-lookup"><span data-stu-id="701d1-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="701d1-147">Un conjunto de etiquetas puede basarse en pares de BYTEs, palabras, DWORD, LARGEINT, SYSTEMTIME y de etiquetas de bits.</span><span class="sxs-lookup"><span data-stu-id="701d1-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="701d1-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="701d1-148">Requirements</span></span>



| <span data-ttu-id="701d1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="701d1-149">Requirement</span></span> | <span data-ttu-id="701d1-150">Value</span><span class="sxs-lookup"><span data-stu-id="701d1-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="701d1-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="701d1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="701d1-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="701d1-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="701d1-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="701d1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="701d1-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="701d1-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="701d1-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="701d1-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="701d1-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="701d1-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="701d1-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="701d1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701d1-158">BIT con etiqueta \_</span><span class="sxs-lookup"><span data-stu-id="701d1-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="701d1-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="701d1-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




