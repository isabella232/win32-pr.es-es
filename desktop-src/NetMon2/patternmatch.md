---
description: La estructura PATTERNMATCH define los elementos de patrón que se usan para evaluar un marco.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Estructura PATTERNMATCH (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002236"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="4ae2e-103">Estructura PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="4ae2e-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="4ae2e-104">La estructura **PATTERNMATCH** define los elementos de patrón que se usan para evaluar un marco.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ae2e-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="4ae2e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ae2e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ae2e-107">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="4ae2e-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4ae2e-108">Marcas de coincidencia de patrones:</span><span class="sxs-lookup"><span data-stu-id="4ae2e-108">Pattern match flags:</span></span>



| <span data-ttu-id="4ae2e-109">Value</span><span class="sxs-lookup"><span data-stu-id="4ae2e-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="4ae2e-110">Significado</span><span class="sxs-lookup"><span data-stu-id="4ae2e-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="4ae2e-111"><dt>**Patrón \_ de Marcas de coincidencia \_ \_ no**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="4ae2e-112">Cuando se establece, esta marca conserva los fotogramas que no tienen el patrón especificado en el lugar adecuado.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="4ae2e-113"><dt>**Patrón \_ de Marcas de coincidencia \_ \_ Puerto \_ especificado**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="4ae2e-114">Busca un valor de número de puerto.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="4ae2e-115">**OffsetBasis**</span><span class="sxs-lookup"><span data-stu-id="4ae2e-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="4ae2e-116">Tipos de desplazamiento, que pueden ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ae2e-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="4ae2e-117">Value</span><span class="sxs-lookup"><span data-stu-id="4ae2e-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="4ae2e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="4ae2e-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="4ae2e-119"><dt>**DESPLAZAMIENTO \_ \_ en relación \_ con el \_ marco**</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="4ae2e-120">Establece un desplazamiento, en bytes, con respecto al inicio del marco.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="4ae2e-121"><dt>**DESPLAZAMIENTO \_ \_ en relación \_ con \_ el \_ Protocolo efectivo**</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="4ae2e-122">Establece un desplazamiento, en bytes, con respecto al inicio del Protocolo al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="4ae2e-123"><dt>**DESPLAZAMIENTO \_ \_ de base con respecto \_ a \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="4ae2e-124">Establece un desplazamiento, en bytes, solo con respecto a IPX.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="4ae2e-125"><dt>**\_base \_ de desplazamiento relativa \_ a \_ IP**</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="4ae2e-126">Establece un desplazamiento, en bytes, solo con respecto a IP.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="4ae2e-127">**Puerto**</span><span class="sxs-lookup"><span data-stu-id="4ae2e-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="4ae2e-128">Valor de puerto, si se especifica.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ae2e-129">**Offset**</span><span class="sxs-lookup"><span data-stu-id="4ae2e-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="4ae2e-130">Desplazamiento, en bytes, con respecto al **OffsetBasis**.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="4ae2e-131">**Duración**</span><span class="sxs-lookup"><span data-stu-id="4ae2e-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="4ae2e-132">Longitud del patrón coincidente.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="4ae2e-133">**PatternToMatch**</span><span class="sxs-lookup"><span data-stu-id="4ae2e-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="4ae2e-134">Patrón que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ae2e-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ae2e-135">Remarks</span></span>

<span data-ttu-id="4ae2e-136">Esta estructura se usa para construir un filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="4ae2e-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="4ae2e-137">Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4ae2e-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="4ae2e-138">Un filtro de captura puede contener hasta cuatro estructuras **PATTERNMATCH** .</span><span class="sxs-lookup"><span data-stu-id="4ae2e-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae2e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae2e-139">Requirements</span></span>



| <span data-ttu-id="4ae2e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae2e-140">Requirement</span></span> | <span data-ttu-id="4ae2e-141">Value</span><span class="sxs-lookup"><span data-stu-id="4ae2e-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae2e-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ae2e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae2e-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ae2e-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4ae2e-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ae2e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae2e-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ae2e-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ae2e-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ae2e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ae2e-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae2e-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae2e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ae2e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae2e-149">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="4ae2e-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




