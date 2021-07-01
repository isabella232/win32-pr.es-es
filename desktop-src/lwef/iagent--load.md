---
title: Carga de IAgent
description: Carga de IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120938"
---
# <a name="iagentload"></a><span data-ttu-id="a1833-103">IAgent::Load</span><span class="sxs-lookup"><span data-stu-id="a1833-103">IAgent::Load</span></span>

<span data-ttu-id="a1833-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1833-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="a1833-105">Carga un carácter en la [**colección**](./iagent.md) Caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1833-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="a1833-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a1833-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a1833-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="a1833-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="a1833-108">Tipo de datos variante que debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1833-108">A variant datatype that must be one of the following:</span></span>



| <span data-ttu-id="a1833-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a1833-109">Value</span></span>           | <span data-ttu-id="a1833-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1833-110">Description</span></span>                                                                      |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a1833-111">*Especarchivo*</span><span class="sxs-lookup"><span data-stu-id="a1833-111">*filespec*</span></span> | <span data-ttu-id="a1833-112">Ubicación del archivo local del archivo de definición del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="a1833-112">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="a1833-113">*URL*</span><span class="sxs-lookup"><span data-stu-id="a1833-113">*URL*</span></span>      | <span data-ttu-id="a1833-114">Dirección HTTP del archivo de definición del carácter.</span><span class="sxs-lookup"><span data-stu-id="a1833-114">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="a1833-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="a1833-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a1833-116">Dirección de una variable que recibe el identificador del carácter.</span><span class="sxs-lookup"><span data-stu-id="a1833-116">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="a1833-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="a1833-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="a1833-118">Dirección de una variable que recibe el identificador [**de solicitud**](load-method.md) de carga.</span><span class="sxs-lookup"><span data-stu-id="a1833-118">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="a1833-119">Puede cargar caracteres desde el subdirectorio de Microsoft Agent especificando una ruta de acceso relativa (una que no incluya dos puntos ni un carácter de barra diagonal inicial).</span><span class="sxs-lookup"><span data-stu-id="a1833-119">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="a1833-120">Esto prefida la ruta de acceso con el directorio de caracteres del Agente (ubicado en el directorio %windows% \\ msagent localizado).</span><span class="sxs-lookup"><span data-stu-id="a1833-120">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="a1833-121">También puede usar una dirección relativa para especificar su propio directorio en el directorio Chars del agente.</span><span class="sxs-lookup"><span data-stu-id="a1833-121">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="a1833-122">No se puede cargar el mismo carácter (un carácter con el mismo GUID) más de una vez desde una sola conexión.</span><span class="sxs-lookup"><span data-stu-id="a1833-122">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="a1833-123">Del mismo modo, no se puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una sola conexión, porque el carácter predeterminado podría ser el mismo que el otro carácter.</span><span class="sxs-lookup"><span data-stu-id="a1833-123">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="a1833-124">Sin embargo, puede crear otra conexión (mediante CoCreateInstance) y cargar el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="a1833-124">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="a1833-125">El proveedor de datos de Microsoft Agent admite la carga de datos de caracteres almacenados como un único archivo estructurado (. ACS) con datos de caracteres y datos de animación juntos, o como datos de caracteres independientes (. ACF) y animación (. ACA).</span><span class="sxs-lookup"><span data-stu-id="a1833-125">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="a1833-126">Por lo general, use la estructura única . Archivo de ACS para cargar un carácter que se almacena en una unidad de disco local o red y al que se accede mediante el protocolo de archivos convencional (por ejemplo, unc pathnames).</span><span class="sxs-lookup"><span data-stu-id="a1833-126">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="a1833-127">Use el independiente . ACF y . Archivos ACA cuando quiera cargar los archivos de animación individualmente desde un sitio remoto al que se tiene acceso mediante el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1833-127">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="a1833-128">Para. Los archivos de ACS, mediante [**el método Load**](load-method.md) proporcionan acceso a las animaciones de un carácter; Una vez cargado, puede usar el [**método Play**](play-method.md) para animar el carácter.</span><span class="sxs-lookup"><span data-stu-id="a1833-128">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="a1833-129">Para. Archivos ACF, también se usa el [**método Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para cargar datos de animación.</span><span class="sxs-lookup"><span data-stu-id="a1833-129">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="a1833-130">El **método Load** no admite la descarga de . Archivos de ACS desde un sitio HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1833-130">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="a1833-131">La carga de un carácter no muestra automáticamente el carácter.</span><span class="sxs-lookup"><span data-stu-id="a1833-131">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="a1833-132">Use primero [**el método Show**](show-method.md) para que el carácter sea visible.</span><span class="sxs-lookup"><span data-stu-id="a1833-132">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 