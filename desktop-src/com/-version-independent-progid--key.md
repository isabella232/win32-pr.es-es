---
title: Clave ProgID independiente de la versión
description: Asocia un ProgID a un CLSID. Esta clave se usa para determinar la versión más reciente de una aplicación de objeto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488801"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="19bb0-104">Clave ProgID independiente de la versión</span><span class="sxs-lookup"><span data-stu-id="19bb0-104">version-independent ProgID Key</span></span>

<span data-ttu-id="19bb0-105">Asocia un ProgID a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="19bb0-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="19bb0-106">Esta clave se usa para determinar la versión más reciente de una aplicación de objeto.</span><span class="sxs-lookup"><span data-stu-id="19bb0-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="19bb0-107">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="19bb0-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="19bb0-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19bb0-108">Remarks</span></span>

<span data-ttu-id="19bb0-109">La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.</span><span class="sxs-lookup"><span data-stu-id="19bb0-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="19bb0-110">El formato de <*ProgID independiente* de la versión> es <*programa*>. <*componente*>, separados por puntos, sin espacios y sin número de versión.</span><span class="sxs-lookup"><span data-stu-id="19bb0-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="19bb0-111">El ProgID independiente de la versión, como el ProgID, se puede registrar con un nombre legible.</span><span class="sxs-lookup"><span data-stu-id="19bb0-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="19bb0-112">*ProgID* es el ProgID de la versión instalada más reciente de la clase.</span><span class="sxs-lookup"><span data-stu-id="19bb0-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="19bb0-113">Las aplicaciones deben registrar un identificador de programación independiente de la versión en la clave *ProgID independiente de la versión* .</span><span class="sxs-lookup"><span data-stu-id="19bb0-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="19bb0-114">El ProgID independiente de la versión hace referencia a la clase de la aplicación y no cambia de la versión a la versión, sino a la constante restante en todos los versionsâ, por ejemplo, el documento de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="19bb0-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="19bb0-115">Se usa con lenguajes de macros y hace referencia a la versión instalada actualmente de la clase de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19bb0-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="19bb0-116">El ProgID independiente de la versión debe corresponder al nombre de la versión más reciente de la aplicación de objeto.</span><span class="sxs-lookup"><span data-stu-id="19bb0-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="19bb0-117">Por ejemplo, el ProgID independiente de la versión se utiliza cuando una aplicación contenedora crea un gráfico o una tabla con un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="19bb0-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="19bb0-118">En esta situación, la aplicación puede usar el ProgID independiente de la versión para determinar la versión más reciente de la aplicación de objeto necesaria.</span><span class="sxs-lookup"><span data-stu-id="19bb0-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="19bb0-119">El ProgID independiente de la versión se almacena y mantiene únicamente en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19bb0-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="19bb0-120">Cuando se proporciona el ProgID independiente de la versión, la función [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) devuelve el CLSID de la versión actual.</span><span class="sxs-lookup"><span data-stu-id="19bb0-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="19bb0-121">Puede usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para realizar la conversión entre estas dos representaciones.</span><span class="sxs-lookup"><span data-stu-id="19bb0-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="19bb0-122">Puede usar [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) o [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) para cambiar el identificador a una cadena que se pueda mostrar.</span><span class="sxs-lookup"><span data-stu-id="19bb0-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="19bb0-123">Si no se utiliza un controlador personalizado, la entrada debe establecerse en OLE32.DLL, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="19bb0-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="19bb0-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19bb0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19bb0-125">**CLSIDFromProgID**</span><span class="sxs-lookup"><span data-stu-id="19bb0-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="19bb0-126">**ProgIDFromCLSID**</span><span class="sxs-lookup"><span data-stu-id="19bb0-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="19bb0-127"><ProgID> Clave</span><span class="sxs-lookup"><span data-stu-id="19bb0-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 




