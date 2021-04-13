---
description: La función de exportación ParserAutoInstallInfo identifica el analizador o los analizadores que se encuentran en un archivo DLL. ParserAutoInstallInfo debe implementarse en todos los archivos dll de analizador.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Función de devolución de llamada ParserAutoInstallInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360147"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="983e8-104">Función de devolución de llamada ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="983e8-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="983e8-105">La función de exportación **ParserAutoInstallInfo** identifica el analizador o los analizadores que se encuentran en un archivo dll.</span><span class="sxs-lookup"><span data-stu-id="983e8-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="983e8-106">**ParserAutoInstallInfo** debe implementarse en todos los archivos dll de analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="983e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="983e8-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="983e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="983e8-108">Parameters</span></span>

<span data-ttu-id="983e8-109">Esta función de devolución de llamada no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="983e8-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="983e8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="983e8-110">Return value</span></span>

<span data-ttu-id="983e8-111">Si la función se realiza correctamente, el valor devuelto es una estructura [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) que describe los analizadores en el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="983e8-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="983e8-112">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="983e8-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="983e8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="983e8-113">Remarks</span></span>

<span data-ttu-id="983e8-114">Cuando Monitor de red se carga por primera vez, llama a **ParserAutoInstallInfo** (si existe) para instalar automáticamente cada analizador y, a continuación, enumera todos los archivos DLL del analizador en el subdirectorio del analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="983e8-115">La información devuelta en la estructura **PF \_ PARSERDLLINFO** incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="983e8-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="983e8-116">El número de analizadores en el archivo DLL (normalmente uno).</span><span class="sxs-lookup"><span data-stu-id="983e8-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="983e8-117">El nombre y una breve descripción del protocolo que detecta cada analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="983e8-118">Un archivo de ayuda opcional para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="983e8-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="983e8-119">Los protocolos que preceden a cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="983e8-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="983e8-120">Los protocolos que siguen a cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="983e8-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="983e8-121">Cada DLL del analizador debe contener un analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="983e8-122">Sin embargo, Monitor de red le permite crear un archivo DLL que contiene más de un analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="983e8-123">Por ejemplo, tcpip.dll es una Monitor de red DLL con más de un analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="983e8-124">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="983e8-124">For information on</span></span>                                               | <span data-ttu-id="983e8-125">Vea</span><span class="sxs-lookup"><span data-stu-id="983e8-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="983e8-126">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="983e8-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="983e8-127">Analizadores</span><span class="sxs-lookup"><span data-stu-id="983e8-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="983e8-128">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="983e8-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="983e8-129">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="983e8-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="983e8-130">Cómo implementar **ParserAutoInstallInfo**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="983e8-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="983e8-131">Implementación de ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="983e8-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="983e8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="983e8-132">Requirements</span></span>



| <span data-ttu-id="983e8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="983e8-133">Requirement</span></span> | <span data-ttu-id="983e8-134">Value</span><span class="sxs-lookup"><span data-stu-id="983e8-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="983e8-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="983e8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="983e8-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="983e8-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="983e8-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="983e8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="983e8-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="983e8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="983e8-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="983e8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="983e8-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="983e8-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983e8-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="983e8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983e8-142">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="983e8-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




