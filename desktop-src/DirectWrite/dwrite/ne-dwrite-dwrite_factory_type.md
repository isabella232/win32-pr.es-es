---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Especifica el tipo de objeto de generador de DirectWrite.
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
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2020
ms.locfileid: "104078792"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="faf7c-103">Enumeración DWRITE_FACTORY_TYPE (DWRITE. h)</span><span class="sxs-lookup"><span data-stu-id="faf7c-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="faf7c-104">Especifica el tipo de objeto de generador de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="faf7c-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="faf7c-105">Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="faf7c-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="faf7c-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="faf7c-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="faf7c-107">Para obtener más información y ejemplos de código, consulte [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="faf7c-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="faf7c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faf7c-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a><span data-ttu-id="faf7c-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="faf7c-109">Constants</span></span>

| <span data-ttu-id="faf7c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="faf7c-110">Name</span></span> | <span data-ttu-id="faf7c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="faf7c-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="faf7c-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="faf7c-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="faf7c-113">Indica que el generador de DirectWrite es un generador compartido y que permite la reutilización de datos de fuentes almacenados en memoria caché en varios componentes en proceso.</span><span class="sxs-lookup"><span data-stu-id="faf7c-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="faf7c-114">Estos generadores también aprovechan los componentes de almacenamiento en caché de fuentes entre procesos para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="faf7c-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="faf7c-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="faf7c-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="faf7c-116">Indica que el objeto de generador de DirectWrite está aislado.</span><span class="sxs-lookup"><span data-stu-id="faf7c-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="faf7c-117">Los objetos creados a partir del generador aislado no interactúan con el estado interno de DirectWrite desde otros componentes.</span><span class="sxs-lookup"><span data-stu-id="faf7c-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="faf7c-118">DWRITE_FACTORY_TYPE_RESTRICTED</span><span class="sxs-lookup"><span data-stu-id="faf7c-118">DWRITE_FACTORY_TYPE_RESTRICTED</span></span> | <span data-ttu-id="faf7c-119">Los objetos creados a partir de un generador restringido no usan ni modifican los datos de estado interno o almacenados en caché usados por otros generadores.</span><span class="sxs-lookup"><span data-stu-id="faf7c-119">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="faf7c-120">Además, la colección de fuentes del sistema solo contiene fuentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="faf7c-120">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="faf7c-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="faf7c-121">Examples</span></span>

<span data-ttu-id="faf7c-122">Consulte el tema de [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="faf7c-122">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="faf7c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faf7c-123">Remarks</span></span>

<span data-ttu-id="faf7c-124">Un objeto de generador de DirectWrite contiene información sobre su estado interno, como el registro del cargador de fuentes y los datos de fuentes en caché.</span><span class="sxs-lookup"><span data-stu-id="faf7c-124">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="faf7c-125">En la mayoría de los casos, debe usar el objeto de generador compartido, ya que permite que varios componentes que usan DirectWrite compartan información interna de estado de DirectWrite, lo que reduce el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="faf7c-125">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="faf7c-126">Sin embargo, hay casos en los que es deseable reducir el impacto de un componente en el resto del proceso, como un complemento de un origen que no es de confianza, mediante el espacio aislado y el aislamiento del resto de los componentes del proceso.</span><span class="sxs-lookup"><span data-stu-id="faf7c-126">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="faf7c-127">En tales casos, debe usar un generador aislado para el componente de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="faf7c-127">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="faf7c-128">Un generador restringido está más bloqueado que un generador aislado.</span><span class="sxs-lookup"><span data-stu-id="faf7c-128">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="faf7c-129">No interactúa de ningún modo con una memoria caché de fuentes entre procesos ni persistentes.</span><span class="sxs-lookup"><span data-stu-id="faf7c-129">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="faf7c-130">Además, la colección de fuentes del sistema devuelta desde este generador solo incluye fuentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="faf7c-130">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="faf7c-131">Si pasa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versión de DWRITE anterior a DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) devuelve **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="faf7c-131">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf7c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf7c-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="faf7c-133">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="faf7c-133">**Minimum supported client**</span></span> | <span data-ttu-id="faf7c-134">Windows 10, versión preliminar de Project reunion 0,1 [aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="faf7c-134">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="faf7c-135">**Header**</span><span class="sxs-lookup"><span data-stu-id="faf7c-135">**Header**</span></span> | <span data-ttu-id="faf7c-136">dwrite. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="faf7c-136">dwrite.h (include dwrite_core.h)</span></span> |
