---
description: La \_ estructura PF HANDOFFENTRY define un protocolo que monitor de red agrega al conjunto de entrega de un analizador.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Estructura de PF_HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678132"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="bcf9c-103">\_Estructura PF HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="bcf9c-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="bcf9c-104">La estructura **PF \_ HANDOFFENTRY** define un protocolo que monitor de red agrega al conjunto de entrega de un analizador.</span><span class="sxs-lookup"><span data-stu-id="bcf9c-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf9c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcf9c-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="bcf9c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bcf9c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bcf9c-107">**szIniFile**</span><span class="sxs-lookup"><span data-stu-id="bcf9c-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="bcf9c-108">Nombre del archivo INI asociado al Protocolo.</span><span class="sxs-lookup"><span data-stu-id="bcf9c-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bcf9c-109">**szIniSection**</span><span class="sxs-lookup"><span data-stu-id="bcf9c-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="bcf9c-110">Etiqueta de sección dentro del archivo INI.</span><span class="sxs-lookup"><span data-stu-id="bcf9c-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="bcf9c-111">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="bcf9c-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="bcf9c-112">Nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="bcf9c-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bcf9c-113">**dwHandOffValue**</span><span class="sxs-lookup"><span data-stu-id="bcf9c-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="bcf9c-114">Valor asociado al Protocolo.</span><span class="sxs-lookup"><span data-stu-id="bcf9c-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bcf9c-115">**ValueFormatBase**</span><span class="sxs-lookup"><span data-stu-id="bcf9c-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="bcf9c-116">Base numérica del valor del protocolo que se especifica en **dwHandOffValue**.</span><span class="sxs-lookup"><span data-stu-id="bcf9c-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="bcf9c-117">La función **ValueFormatBase** debe establecerse en uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bcf9c-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="bcf9c-118">Value</span><span class="sxs-lookup"><span data-stu-id="bcf9c-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="bcf9c-119">Significado</span><span class="sxs-lookup"><span data-stu-id="bcf9c-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="bcf9c-120"><dt>**BASE de formato de valor de entrega \_ \_ \_ \_ desconocida**</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9c-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="bcf9c-121">Base desconocida</span><span class="sxs-lookup"><span data-stu-id="bcf9c-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="bcf9c-122"><dt>**formato de valor de entrega \_ \_ \_ \_ decimal base**</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9c-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="bcf9c-123">Base decimal</span><span class="sxs-lookup"><span data-stu-id="bcf9c-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="bcf9c-124"><dt>**formato de valor de entrega \_ \_ \_ \_ hexadecimal base**</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9c-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="bcf9c-125">Base hexadecimal</span><span class="sxs-lookup"><span data-stu-id="bcf9c-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcf9c-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcf9c-126">Remarks</span></span>

<span data-ttu-id="bcf9c-127">Se usa una matriz de las estructuras **PF \_ HANDOFFENTRY** en la estructura [PF \_ HANDOFFSET](pf-handoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="bcf9c-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf9c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcf9c-128">Requirements</span></span>



| <span data-ttu-id="bcf9c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf9c-129">Requirement</span></span> | <span data-ttu-id="bcf9c-130">Value</span><span class="sxs-lookup"><span data-stu-id="bcf9c-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf9c-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf9c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf9c-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bcf9c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bcf9c-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf9c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf9c-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bcf9c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bcf9c-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcf9c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf9c-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9c-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf9c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcf9c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf9c-138">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="bcf9c-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 




