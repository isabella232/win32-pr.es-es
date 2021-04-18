---
title: modificador/prefix
description: El modificador/prefix indica al compilador de MIDL que agregue cadenas de prefijo a los nombres de rutina de código auxiliar de cliente o servidor.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix modificador MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532739"
---
# <a name="prefix-switch"></a><span data-ttu-id="72469-104">modificador/prefix</span><span class="sxs-lookup"><span data-stu-id="72469-104">/prefix switch</span></span>

<span data-ttu-id="72469-105">El modificador **/prefix** indica al compilador de MIDL que agregue cadenas de prefijo a los nombres de rutina de código auxiliar de cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="72469-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="72469-106">Se puede usar para permitir que un único programa sea un cliente y un servidor de la misma interfaz, sin que los nombres de las rutinas del cliente y del servidor entren en conflicto entre sí.</span><span class="sxs-lookup"><span data-stu-id="72469-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="72469-107">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="72469-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="72469-108"><span id="client"></span><span id="CLIENT"></span>cliente \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="72469-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="72469-109">Afecta únicamente a los nombres de rutina de código auxiliar de cliente.</span><span class="sxs-lookup"><span data-stu-id="72469-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="72469-110"><span id="cstub"></span><span id="CSTUB"></span>cstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="72469-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="72469-111">Igual que el *cliente*.</span><span class="sxs-lookup"><span data-stu-id="72469-111">Same as *client*.</span></span> <span data-ttu-id="72469-112">Afecta únicamente a los nombres de rutina de código auxiliar de cliente.</span><span class="sxs-lookup"><span data-stu-id="72469-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="72469-113"><span id="server"></span><span id="SERVER"></span>servidor \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="72469-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="72469-114">Afecta únicamente a los nombres de rutinas a los que llama la rutina de código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="72469-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="72469-115"><span id="sstub"></span><span id="SSTUB"></span>sstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="72469-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="72469-116">Igual que el *servidor*.</span><span class="sxs-lookup"><span data-stu-id="72469-116">Same as *server*.</span></span> <span data-ttu-id="72469-117">Afecta únicamente a los nombres de rutinas a los que llama la rutina de código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="72469-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="72469-118"><span id="switch"></span><span id="SWITCH"></span>cambiar \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="72469-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="72469-119">Afecta a un prototipo adicional agregado al archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="72469-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="72469-120"><span id="all"></span><span id="ALL"></span>todo \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="72469-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="72469-121">Afecta a los nombres de rutina de código auxiliar de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="72469-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72469-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72469-122">Remarks</span></span>

<span data-ttu-id="72469-123">Si el prefijo de las rutinas del lado cliente es diferente del prefijo para las rutinas del lado servidor, el archivo de encabezado generado tendrá tanto prototipos de rutina del lado cliente como prototipos de rutina del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="72469-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="72469-124">El modificador **/prefix** resulta útil cuando se utiliza un único archivo de encabezado con códigos auxiliares de varias ejecuciones del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="72469-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="72469-125">Esto fuerza los prototipos de rutina adicionales en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="72469-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="72469-126">En todos los casos, el cliente, el servidor y los prefijos de conmutador invalidarán un prefijo ALL.</span><span class="sxs-lookup"><span data-stu-id="72469-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="72469-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="72469-127">Examples</span></span>

<span data-ttu-id="72469-128">**cliente de/Prefix de MIDL "c \_ " Server "s \_ "**</span><span class="sxs-lookup"><span data-stu-id="72469-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="72469-129">**MIDL/prefix All "Moo \_ "**</span><span class="sxs-lookup"><span data-stu-id="72469-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="72469-130">**cliente de/prefix MIDL "corteza \_ "**</span><span class="sxs-lookup"><span data-stu-id="72469-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="72469-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="72469-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72469-132">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="72469-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




