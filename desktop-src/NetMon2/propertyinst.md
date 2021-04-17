---
description: La estructura PROPERTYINST define una instancia de una propiedad en un elemento de datos reconocidos. Monitor de red asigna y rellena una estructura PROPERTYINST cuando una propiedad se adjunta a la captura.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Estructura PROPERTYINST (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666990"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="32982-104">Estructura PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="32982-104">PROPERTYINST structure</span></span>

<span data-ttu-id="32982-105">La estructura **PROPERTYINST** define una instancia de una propiedad en un elemento de datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="32982-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="32982-106">Monitor de red asigna y rellena una estructura **PROPERTYINST** cuando una propiedad se adjunta a la captura.</span><span class="sxs-lookup"><span data-stu-id="32982-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="32982-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32982-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="32982-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="32982-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="32982-109">**lpPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="32982-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="32982-110">Puntero a la estructura [PROPERTYINFO](propertyinfo.md) que define la propiedad.</span><span class="sxs-lookup"><span data-stu-id="32982-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="32982-111">**szPropertyText**</span><span class="sxs-lookup"><span data-stu-id="32982-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="32982-112">Puntero a una cadena que se muestra en el panel de detalles de la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="32982-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="32982-113">**lpData**</span><span class="sxs-lookup"><span data-stu-id="32982-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="32982-114">Puntero al inicio de los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="32982-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="32982-115">El analizador determina dónde se inician los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="32982-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="32982-116">**lpByte**</span><span class="sxs-lookup"><span data-stu-id="32982-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="32982-117">Puntero a los datos de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="32982-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="32982-118">**lpWord**</span><span class="sxs-lookup"><span data-stu-id="32982-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="32982-119">Puntero a los datos de la **palabra** .</span><span class="sxs-lookup"><span data-stu-id="32982-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="32982-120">**lpDword**</span><span class="sxs-lookup"><span data-stu-id="32982-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="32982-121">Puntero a los datos **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="32982-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="32982-122">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="32982-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="32982-123">Puntero a los datos de [**LARGEINT**](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="32982-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="32982-124">**lpSysTime**</span><span class="sxs-lookup"><span data-stu-id="32982-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="32982-125">Puntero a los datos [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="32982-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="32982-126">**lpPropertyInstEx**</span><span class="sxs-lookup"><span data-stu-id="32982-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="32982-127">Puntero a una estructura [PROPERTYINSTEX](propertyinstex.md) .</span><span class="sxs-lookup"><span data-stu-id="32982-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="32982-128">El miembro **lpPropertyInstEx** se usa solo cuando se llama a [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span><span class="sxs-lookup"><span data-stu-id="32982-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="32982-129">Si se usa **lpPropertyInstEx** , debe establecer el miembro **DATALENGTH** en 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="32982-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="32982-130">**DataLength**</span><span class="sxs-lookup"><span data-stu-id="32982-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="32982-131">Longitud de los datos de esta instancia de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="32982-131">Data length for this instance of the property.</span></span> <span data-ttu-id="32982-132">Si el miembro **lpPropertyInstEx** apunta a una estructura [**PROPERTYINSTEX**](propertyinstex.md) , debe establecer **DATALENGTH** en 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="32982-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="32982-133">**Level**</span><span class="sxs-lookup"><span data-stu-id="32982-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="32982-134">Información de nivel.</span><span class="sxs-lookup"><span data-stu-id="32982-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="32982-135">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="32982-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="32982-136">Identificador de contexto del archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="32982-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="32982-137">**IFlags**</span><span class="sxs-lookup"><span data-stu-id="32982-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="32982-138">Marca de condición de error.</span><span class="sxs-lookup"><span data-stu-id="32982-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32982-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32982-139">Remarks</span></span>

<span data-ttu-id="32982-140">La estructura **PROPERTYINST** define una instancia de una propiedad adjunta.</span><span class="sxs-lookup"><span data-stu-id="32982-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="32982-141">El analizador accede a la estructura **PROPERTYINST** a través de varias funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="32982-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="32982-142">Por ejemplo, cuando se llama a la función [**FormatPropertyInstance**](formatpropertyinstance.md) para dar formato a los datos de una propiedad, modifica el miembro **szPropertyText** de la estructura **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="32982-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="32982-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32982-143">Requirements</span></span>



| <span data-ttu-id="32982-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="32982-144">Requirement</span></span> | <span data-ttu-id="32982-145">Value</span><span class="sxs-lookup"><span data-stu-id="32982-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32982-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32982-146">Minimum supported client</span></span><br/> | <span data-ttu-id="32982-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32982-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="32982-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32982-148">Minimum supported server</span></span><br/> | <span data-ttu-id="32982-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32982-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="32982-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32982-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="32982-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="32982-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32982-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="32982-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32982-153">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="32982-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="32982-154">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="32982-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

