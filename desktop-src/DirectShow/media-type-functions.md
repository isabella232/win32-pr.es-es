---
description: Las clases base de DirectShow proporcionan funciones auxiliares para controlar la \_ estructura de tipo de medio am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funciones de tipo de medio (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689930"
---
# <a name="media-type-functions"></a><span data-ttu-id="50ec7-103">Funciones de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="50ec7-103">Media Type Functions</span></span>

<span data-ttu-id="50ec7-104">Las clases base de DirectShow proporcionan funciones auxiliares para controlar la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="50ec7-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="50ec7-105">La estructura de **\_ \_ tipo de medio am** contiene un puntero (el miembro **pbFormat** ) a otro bloque de memoria, que se denomina *bloque de formato*.</span><span class="sxs-lookup"><span data-stu-id="50ec7-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="50ec7-106">Al trabajar con esta estructura, por lo tanto, debe tener cuidado con la asignación de memoria para evitar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="50ec7-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="50ec7-107">Las siguientes funciones asignan memoria:</span><span class="sxs-lookup"><span data-stu-id="50ec7-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="50ec7-108">**CreateMediaType** asigna una nueva estructura de **\_ \_ tipo de medio am** y el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="50ec7-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="50ec7-109">**CopyMediaType** copia en una estructura **de \_ \_ tipo de medio am** existente, pero asigna el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="50ec7-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="50ec7-110">**CreateAudioMediaType** Inicializa una estructura de **\_ \_ tipo de medio am** existente y, opcionalmente, asigna el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="50ec7-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="50ec7-111">Las siguientes funciones liberan memoria:</span><span class="sxs-lookup"><span data-stu-id="50ec7-111">The following functions free memory:</span></span>

-   <span data-ttu-id="50ec7-112">**FreeMediaType** libera el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="50ec7-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="50ec7-113">**DeleteMediaType** libera una estructura **de \_ \_ tipo de medio am** , incluido el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="50ec7-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="50ec7-114">Función</span><span class="sxs-lookup"><span data-stu-id="50ec7-114">Function</span></span>                                             | <span data-ttu-id="50ec7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="50ec7-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50ec7-116">**CopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="50ec7-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="50ec7-117">Copia una estructura de **tipo de \_ medio \_ AM** asignada a tareas.</span><span class="sxs-lookup"><span data-stu-id="50ec7-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="50ec7-118">**CreateAudioMediaType**</span><span class="sxs-lookup"><span data-stu-id="50ec7-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="50ec7-119">Inicializa una estructura de tipo de archivo multimedia a partir de una estructura de formato de onda.</span><span class="sxs-lookup"><span data-stu-id="50ec7-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="50ec7-120">**CreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="50ec7-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="50ec7-121">Asigna e inicializa una estructura de **tipo de \_ medio \_ AM** a partir de una estructura de **\_ \_ tipo de medio am** existente.</span><span class="sxs-lookup"><span data-stu-id="50ec7-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="50ec7-122">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="50ec7-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="50ec7-123">Elimina una estructura de **\_ \_ tipo de medio am** asignada por tarea.</span><span class="sxs-lookup"><span data-stu-id="50ec7-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="50ec7-124">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="50ec7-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="50ec7-125">Libera una estructura de **\_ \_ tipo de medio am** asignada por tarea de la memoria.</span><span class="sxs-lookup"><span data-stu-id="50ec7-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="50ec7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50ec7-126">Requirements</span></span>



| <span data-ttu-id="50ec7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="50ec7-127">Requirement</span></span> | <span data-ttu-id="50ec7-128">Value</span><span class="sxs-lookup"><span data-stu-id="50ec7-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ec7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50ec7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="50ec7-130"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50ec7-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="50ec7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50ec7-131">Library</span></span><br/> | <dl> <span data-ttu-id="50ec7-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="50ec7-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




