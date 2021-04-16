---
description: Proporciona una línea en el panel superior de la Visor de eventos que actúa como contenedor para todos los datos posibles insertados en una columna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Estructura NMCOLUMNVARIANT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669833"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="d5609-103">Estructura NMCOLUMNVARIANT</span><span class="sxs-lookup"><span data-stu-id="d5609-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="d5609-104">La estructura **NMCOLUMNVARIANT** proporciona una línea en el panel superior de la visor de eventos que actúa como contenedor para todos los datos posibles insertados en una columna.</span><span class="sxs-lookup"><span data-stu-id="d5609-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5609-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5609-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="d5609-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d5609-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5609-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d5609-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-108">Un valor del tipo de enumeración [**NMCOLUMNTYPE**](nmcolumntype.md) .</span><span class="sxs-lookup"><span data-stu-id="d5609-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d5609-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5609-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-111">valor entero de 8 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d5609-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-113">valor entero de 8 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="d5609-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-115">valor entero sin signo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d5609-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-117">valor entero de 16 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="d5609-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-119">valor entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d5609-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-121">valor entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="d5609-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="d5609-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-123">valor Float de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d5609-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-124">**FrameVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-125">Número de marco.</span><span class="sxs-lookup"><span data-stu-id="d5609-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-126">**YesNoVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-127">Muestra sí o no.</span><span class="sxs-lookup"><span data-stu-id="d5609-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-128">**OnOffVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-129">Muestra activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="d5609-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-130">**TrueFalseVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-131">Muestra true o false.</span><span class="sxs-lookup"><span data-stu-id="d5609-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-132">**MACAddrVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-133">Dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="d5609-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-134">**IPXAddrVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-135">Dirección IPX.</span><span class="sxs-lookup"><span data-stu-id="d5609-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-136">**IPAddrVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-137">Dirección IP.</span><span class="sxs-lookup"><span data-stu-id="d5609-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-138">**VarTimeVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-139">Hora de la variante.</span><span class="sxs-lookup"><span data-stu-id="d5609-139">Variant time.</span></span> <span data-ttu-id="d5609-140">Use **VariantTimetoSystemTime** para convertir a la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5609-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-141">**pStringVal**</span><span class="sxs-lookup"><span data-stu-id="d5609-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="d5609-142">Puntero a una cadena.</span><span class="sxs-lookup"><span data-stu-id="d5609-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5609-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5609-143">Requirements</span></span>



| <span data-ttu-id="d5609-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5609-144">Requirement</span></span> | <span data-ttu-id="d5609-145">Value</span><span class="sxs-lookup"><span data-stu-id="d5609-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d5609-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5609-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d5609-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5609-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d5609-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5609-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d5609-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5609-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d5609-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5609-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5609-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5609-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5609-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5609-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5609-153">**NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="d5609-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 




