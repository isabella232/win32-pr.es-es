---
description: La \_ estructura PF PARSERINFO define un analizador cada vez. En la \_ estructura PF PARSERINFO, se define un analizador mediante la información sobre el protocolo que detecta el analizador.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Estructura de PF_PARSERINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678131"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="0cd83-104">\_Estructura PF PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="0cd83-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="0cd83-105">La estructura **PF \_ PARSERINFO** define un analizador cada vez.</span><span class="sxs-lookup"><span data-stu-id="0cd83-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="0cd83-106">En la estructura **PF \_ PARSERINFO** , se define un analizador mediante la información sobre el protocolo que detecta el analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd83-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cd83-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="0cd83-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cd83-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0cd83-109">**szProtocolName**</span><span class="sxs-lookup"><span data-stu-id="0cd83-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-110">Nombre del protocolo que detecta el analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-111">**szComment**</span><span class="sxs-lookup"><span data-stu-id="0cd83-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-112">Breve descripción del protocolo.</span><span class="sxs-lookup"><span data-stu-id="0cd83-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-113">**szHelpFile**</span><span class="sxs-lookup"><span data-stu-id="0cd83-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-114">Nombre del archivo de ayuda del Protocolo, si existe.</span><span class="sxs-lookup"><span data-stu-id="0cd83-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-115">**pWhoCanPrecedeMe**</span><span class="sxs-lookup"><span data-stu-id="0cd83-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-116">Puntero a una estructura [PF \_ FOLLOWSET](pf-followset.md) que enumera los protocolos que pueden preceder al protocolo que describe la estructura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="0cd83-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="0cd83-117">Monitor de red agrega el protocolo del analizador al [*siguiente conjunto*](f.md) de todos los protocolos del conjunto.</span><span class="sxs-lookup"><span data-stu-id="0cd83-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-118">**pWhoCanFollowMe**</span><span class="sxs-lookup"><span data-stu-id="0cd83-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-119">Puntero a una estructura de [PF \_ FOLLOWSET](pf-followset.md) que muestra el protocolo que puede seguir el protocolo que describe la estructura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="0cd83-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="0cd83-120">Monitor de red agrega los protocolos del conjunto al [*siguiente conjunto*](f.md) del protocolo del analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-121">**pWhoHandsOffToMe**</span><span class="sxs-lookup"><span data-stu-id="0cd83-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-122">Puntero a una estructura [PF \_ HANDOFFSET](pf-handoffset.md) que se describa en el protocolo que describe la estructura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="0cd83-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="0cd83-123">Monitor de red agrega el protocolo del analizador a los [*conjuntos de entrega*](h.md) de todos los protocolos del conjunto.</span><span class="sxs-lookup"><span data-stu-id="0cd83-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-124">**pWhoDoIHandOffTo**</span><span class="sxs-lookup"><span data-stu-id="0cd83-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-125">Puntero a una estructura de [PF \_ HANDOFFSET](pf-handoffset.md) que enumera los protocolos a los que el protocolo del analizador se entrega.</span><span class="sxs-lookup"><span data-stu-id="0cd83-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="0cd83-126">Monitor de red agrega los protocolos de este conjunto al [*conjunto de entrega*](h.md) del protocolo del analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cd83-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cd83-127">Remarks</span></span>

<span data-ttu-id="0cd83-128">La estructura **PF \_ PARSERINFO** se usa en la estructura **PF \_ PARSERDLLINFO** para proporcionar una descripción de un analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="0cd83-129">Monitor de red usa la descripción del analizador para actualizar el archivo [*Parser.ini*](p.md) y los archivos INI de los analizadores que preceden y siguen al protocolo descrito en la estructura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="0cd83-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="0cd83-130">Un conjunto siguiente especifica los protocolos que siguen a un protocolo.</span><span class="sxs-lookup"><span data-stu-id="0cd83-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="0cd83-131">Monitor de red usa un conjunto de seguimiento cuando el analizador no puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.</span><span class="sxs-lookup"><span data-stu-id="0cd83-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="0cd83-132">En el archivo [*Parser.ini*](p.md) se almacena un conjunto de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="0cd83-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="0cd83-133">Cuando el analizador se instala por primera vez, Monitor de red actualiza el siguiente conjunto de protocolos de analizador que se enumeran en **pWhoCanPrecedeMe** y **pWhoCanFollowMe**.</span><span class="sxs-lookup"><span data-stu-id="0cd83-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="0cd83-134">Un conjunto de entrega especifica los protocolos que siguen a un protocolo.</span><span class="sxs-lookup"><span data-stu-id="0cd83-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="0cd83-135">El analizador utiliza un conjunto de entrega solo cuando el analizador puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.</span><span class="sxs-lookup"><span data-stu-id="0cd83-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="0cd83-136">Un conjunto de entrega se almacena en los archivos INI de cada analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="0cd83-137">Cuando el analizador se instala por primera vez, Monitor de red actualiza el conjunto de entrega de los protocolos de analizador que se enumeran en **pWhoHandsOffToMe** y **pWhoDoIHandOffTo**.</span><span class="sxs-lookup"><span data-stu-id="0cd83-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="0cd83-138">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="0cd83-138">For information on</span></span>                                               | <span data-ttu-id="0cd83-139">Vea</span><span class="sxs-lookup"><span data-stu-id="0cd83-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0cd83-140">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="0cd83-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="0cd83-141">Analizadores</span><span class="sxs-lookup"><span data-stu-id="0cd83-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="0cd83-142">Qué incluyen los conjuntos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0cd83-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="0cd83-143">Especificar un conjunto de seguimiento</span><span class="sxs-lookup"><span data-stu-id="0cd83-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="0cd83-144">Qué contienen los conjuntos de entrega.</span><span class="sxs-lookup"><span data-stu-id="0cd83-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="0cd83-145">Especificar un conjunto de entrega</span><span class="sxs-lookup"><span data-stu-id="0cd83-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="0cd83-146">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="0cd83-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="0cd83-147">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="0cd83-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="0cd83-148">Cómo implementar **ParserAutoInstallInfo**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0cd83-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="0cd83-149">Implementación de ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="0cd83-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="0cd83-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd83-150">Requirements</span></span>



| <span data-ttu-id="0cd83-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd83-151">Requirement</span></span> | <span data-ttu-id="0cd83-152">Value</span><span class="sxs-lookup"><span data-stu-id="0cd83-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd83-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cd83-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd83-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0cd83-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0cd83-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cd83-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd83-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0cd83-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0cd83-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cd83-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cd83-158"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd83-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cd83-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cd83-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd83-160">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="0cd83-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="0cd83-161">PF \_ FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="0cd83-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="0cd83-162">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="0cd83-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="0cd83-163">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="0cd83-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




