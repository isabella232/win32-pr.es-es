---
description: La clase CAutoLock contiene una sección crítica para el ámbito de un bloque de código.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Clase CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670821"
---
# <a name="cautolock-class"></a><span data-ttu-id="155e1-103">Clase CAutoLock</span><span class="sxs-lookup"><span data-stu-id="155e1-103">CAutoLock class</span></span>

<span data-ttu-id="155e1-104">La `CAutoLock` clase contiene una sección crítica para el ámbito de un bloque de código.</span><span class="sxs-lookup"><span data-stu-id="155e1-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="155e1-105">Esta clase funciona junto con la clase [**CCritSec**](ccritsec.md) , que es un contenedor para los objetos de sección críticos.</span><span class="sxs-lookup"><span data-stu-id="155e1-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="155e1-106">El `CAutoLock` constructor bloquea la sección crítica y el destructor la desbloquea.</span><span class="sxs-lookup"><span data-stu-id="155e1-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="155e1-107">Mediante el uso de un `CAutoLock` objeto como variable local, puede bloquear una sección crítica con la garantía de que todas las rutas de acceso de código desbloquearán la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="155e1-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="155e1-108">En el ejemplo de código siguiente se muestra cómo utilizar esta clase:</span><span class="sxs-lookup"><span data-stu-id="155e1-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="155e1-109">Los métodos de esta clase no están diseñados para invalidarse.</span><span class="sxs-lookup"><span data-stu-id="155e1-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="155e1-110">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="155e1-110">Protected Member Variables</span></span>                 | <span data-ttu-id="155e1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="155e1-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="155e1-112">**m \_ Plock**</span><span class="sxs-lookup"><span data-stu-id="155e1-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="155e1-113">Sección crítica para este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="155e1-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="155e1-114">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="155e1-114">Public Methods</span></span>                             | <span data-ttu-id="155e1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="155e1-115">Description</span></span>                                                      |
| [<span data-ttu-id="155e1-116">**CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="155e1-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="155e1-117">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="155e1-117">Constructor method.</span></span> <span data-ttu-id="155e1-118">Bloquea el objeto de sección crítica especificado.</span><span class="sxs-lookup"><span data-stu-id="155e1-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="155e1-119">**~ CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="155e1-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="155e1-120">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="155e1-120">Destructor method.</span></span> <span data-ttu-id="155e1-121">Desbloquea el objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="155e1-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="155e1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="155e1-122">Requirements</span></span>



| <span data-ttu-id="155e1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="155e1-123">Requirement</span></span> | <span data-ttu-id="155e1-124">Value</span><span class="sxs-lookup"><span data-stu-id="155e1-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="155e1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="155e1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="155e1-126"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="155e1-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="155e1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="155e1-127">Library</span></span><br/> | <dl> <span data-ttu-id="155e1-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="155e1-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




