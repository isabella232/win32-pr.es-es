---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Especifica el tipo de objeto de generador DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 85f74d72dc8799a7a3c78603ec0dd5f9c118fdb1
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955008"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="f94f0-103">DWRITE_FACTORY_TYPE enumeración (dwrite.h)</span><span class="sxs-lookup"><span data-stu-id="f94f0-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="f94f0-104">Especifica el tipo de objeto de generador DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f94f0-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f94f0-105">Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f94f0-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="f94f0-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="f94f0-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="f94f0-107">Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](/windows/win32/directwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="f94f0-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="f94f0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f94f0-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="f94f0-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="f94f0-109">Constants</span></span>

| <span data-ttu-id="f94f0-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="f94f0-110">Name</span></span> | <span data-ttu-id="f94f0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f94f0-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="f94f0-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="f94f0-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="f94f0-113">Indica que el generador de DirectWrite es un generador compartido y que permite reutilizar los datos de fuente almacenados en caché en varios componentes en proceso.</span><span class="sxs-lookup"><span data-stu-id="f94f0-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="f94f0-114">Estos generadores también aprovechan los componentes de almacenamiento en caché de fuentes entre procesos para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f94f0-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="f94f0-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="f94f0-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="f94f0-116">Indica que el objeto de generador DirectWrite está aislado.</span><span class="sxs-lookup"><span data-stu-id="f94f0-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="f94f0-117">Los objetos creados a partir del generador aislado no interactúan con el estado interno de DirectWrite de otros componentes.</span><span class="sxs-lookup"><span data-stu-id="f94f0-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="f94f0-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="f94f0-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="f94f0-119">Indica que el objeto de generador DirectWrite está restringido.</span><span class="sxs-lookup"><span data-stu-id="f94f0-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="f94f0-120">Los objetos creados a partir de una factoría restringida no usan ni modifican el estado interno ni los datos almacenados en caché que usan otros generadores.</span><span class="sxs-lookup"><span data-stu-id="f94f0-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="f94f0-121">Además, la colección de fuentes del sistema solo contiene fuentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="f94f0-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="f94f0-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f94f0-122">Examples</span></span>

<span data-ttu-id="f94f0-123">Consulte el [tema de información general de DWriteCore](/windows/win32/directwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="f94f0-123">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="f94f0-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f94f0-124">Remarks</span></span>

<span data-ttu-id="f94f0-125">Un objeto de generador directWrite contiene información sobre su estado interno, como el registro del cargador de fuentes y los datos de fuente almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="f94f0-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="f94f0-126">En la mayoría de los casos, debe usar el objeto de generador compartido, ya que permite que varios componentes que usan DirectWrite compartan información de estado interna de DirectWrite, lo que reduce el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="f94f0-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="f94f0-127">Sin embargo, hay casos en los que es conveniente reducir el impacto de un componente en el resto del proceso, como un complemento de un origen que no es de confianza, mediante el espacio aislado y el aislamiento del resto de los componentes del proceso.</span><span class="sxs-lookup"><span data-stu-id="f94f0-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="f94f0-128">En tales casos, debe usar un generador aislado para el componente de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="f94f0-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="f94f0-129">Una fábrica restringida está más bloqueada que una fábrica aislada.</span><span class="sxs-lookup"><span data-stu-id="f94f0-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="f94f0-130">No interactúa con una caché de fuentes persistentes ni entre procesos de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="f94f0-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="f94f0-131">Además, la colección de fuentes del sistema devuelta desde este generador incluye solo fuentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="f94f0-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="f94f0-132">Si pasa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versión de DWrite anterior a [DWriteCore, DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **devuelve E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="f94f0-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94f0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f94f0-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f94f0-134">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="f94f0-134">**Minimum supported client**</span></span> | <span data-ttu-id="f94f0-135">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="f94f0-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="f94f0-136">**Header**</span><span class="sxs-lookup"><span data-stu-id="f94f0-136">**Header**</span></span> | <span data-ttu-id="f94f0-137">dwrite.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="f94f0-137">dwrite.h (include dwrite_core.h)</span></span> |
