---
description: La \_ estructura PF PARSERDLLINFO define los analizadores ubicados en el archivo DLL del analizador.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Estructura de PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002357"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="edaf8-103">\_Estructura PF PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="edaf8-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="edaf8-104">La estructura **PF \_ PARSERDLLINFO** define los analizadores ubicados en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="edaf8-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="edaf8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edaf8-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="edaf8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="edaf8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="edaf8-107">**nParsers**</span><span class="sxs-lookup"><span data-stu-id="edaf8-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="edaf8-108">Número de analizadores en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="edaf8-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="edaf8-109">**ParserInfo**</span><span class="sxs-lookup"><span data-stu-id="edaf8-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="edaf8-110">Matriz de estructuras [PF \_ PARSERINFO](pf-parserinfo.md) que describen cada analizador en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="edaf8-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="edaf8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edaf8-111">Remarks</span></span>

<span data-ttu-id="edaf8-112">La función de exportación [ParserAutoInstallInfo](parserautoinstallinfo.md) que se implementa en el archivo DLL del analizador devuelve la estructura **PF \_ PARSERDLLINFO** .</span><span class="sxs-lookup"><span data-stu-id="edaf8-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="edaf8-113">La función **ParserAutoInstallInfo** identifica el número de analizadores en el archivo dll y utiliza una matriz de estructuras [PF \_ PARSERINFO](pf-parserinfo.md) para describir cada analizador.</span><span class="sxs-lookup"><span data-stu-id="edaf8-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="edaf8-114">La \_ estructura PF PARSERDLLINFO debe estar asignada mediante **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="edaf8-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="edaf8-115">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="edaf8-115">For information on</span></span>                                               | <span data-ttu-id="edaf8-116">Vea</span><span class="sxs-lookup"><span data-stu-id="edaf8-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="edaf8-117">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="edaf8-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="edaf8-118">Analizadores</span><span class="sxs-lookup"><span data-stu-id="edaf8-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="edaf8-119">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="edaf8-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="edaf8-120">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="edaf8-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="edaf8-121">Cómo implementar **ParserAutoInstallInfo**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="edaf8-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="edaf8-122">Implementación de ParserAutoIstallInfo</span><span class="sxs-lookup"><span data-stu-id="edaf8-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="edaf8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edaf8-123">Requirements</span></span>



| <span data-ttu-id="edaf8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="edaf8-124">Requirement</span></span> | <span data-ttu-id="edaf8-125">Value</span><span class="sxs-lookup"><span data-stu-id="edaf8-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="edaf8-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edaf8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="edaf8-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="edaf8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="edaf8-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edaf8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="edaf8-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edaf8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="edaf8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edaf8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="edaf8-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="edaf8-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edaf8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="edaf8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edaf8-133">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="edaf8-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="edaf8-134">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="edaf8-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 




