---
title: Carga de IAgent
description: Carga de IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995233"
---
# <a name="iagentload"></a><span data-ttu-id="0e983-103">IAgent:: Load</span><span class="sxs-lookup"><span data-stu-id="0e983-103">IAgent::Load</span></span>

<span data-ttu-id="0e983-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e983-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="0e983-105">Carga un carácter en la colección de [**caracteres**](./iagent.md) .</span><span class="sxs-lookup"><span data-stu-id="0e983-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="0e983-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0e983-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0e983-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="0e983-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="0e983-108">Un tipo de datos Variant que debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0e983-108">A variant datatype that must be one of the following:</span></span>



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0e983-109">*filespec*</span><span class="sxs-lookup"><span data-stu-id="0e983-109">*filespec*</span></span> | <span data-ttu-id="0e983-110">Ubicación del archivo local del archivo de definición del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="0e983-110">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="0e983-111">*URL*</span><span class="sxs-lookup"><span data-stu-id="0e983-111">*URL*</span></span>      | <span data-ttu-id="0e983-112">Dirección HTTP del archivo de definición del carácter.</span><span class="sxs-lookup"><span data-stu-id="0e983-112">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="0e983-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="0e983-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="0e983-114">Dirección de una variable que recibe el identificador del carácter.</span><span class="sxs-lookup"><span data-stu-id="0e983-114">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="0e983-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="0e983-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="0e983-116">Dirección de una variable que recibe el identificador de la solicitud de [**carga**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="0e983-116">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="0e983-117">Puede cargar caracteres del subdirectorio del agente de Microsoft especificando una ruta de acceso relativa (una que no incluya un carácter de dos puntos o una barra diagonal inicial).</span><span class="sxs-lookup"><span data-stu-id="0e983-117">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="0e983-118">Esto agrega un prefijo a la ruta de acceso con el directorio de caracteres del agente (ubicado en el directorio% Windows% \\ MSAgent localizado).</span><span class="sxs-lookup"><span data-stu-id="0e983-118">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="0e983-119">También puede usar una dirección relativa para especificar su propio directorio en el directorio chars del agente.</span><span class="sxs-lookup"><span data-stu-id="0e983-119">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="0e983-120">No se puede cargar el mismo carácter (un carácter que tiene el mismo GUID) más de una vez desde una única conexión.</span><span class="sxs-lookup"><span data-stu-id="0e983-120">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="0e983-121">Del mismo modo, no puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una sola conexión, ya que el carácter predeterminado podría ser el mismo que el otro carácter.</span><span class="sxs-lookup"><span data-stu-id="0e983-121">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="0e983-122">Sin embargo, puede crear otra conexión (mediante CoCreateInstance) y cargar el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="0e983-122">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="0e983-123">El proveedor de datos de Microsoft Agent admite la carga de datos de caracteres almacenados como un solo archivo estructurado (. ACS) con datos de caracteres y de animación juntos, o como datos de caracteres independientes (. ACF) y animación (. ACA).</span><span class="sxs-lookup"><span data-stu-id="0e983-123">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="0e983-124">Por lo general, se usa la estructura única. Archivo de ACS para cargar un carácter que está almacenado en una unidad de disco local o en una red y a la que se tiene acceso mediante el protocolo de archivo convencional (como rutas de acceso UNC).</span><span class="sxs-lookup"><span data-stu-id="0e983-124">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="0e983-125">Use la independiente. ACF y. Los archivos ACA cuando desea cargar los archivos de animación de forma individual desde un sitio remoto al que se tiene acceso mediante el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e983-125">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="0e983-126">Para. Los archivos de ACS, mediante el método [**Load**](load-method.md) , proporcionan acceso a las animaciones de un carácter; una vez cargados, puede utilizar el método [**Play**](play-method.md) para animar el carácter.</span><span class="sxs-lookup"><span data-stu-id="0e983-126">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="0e983-127">Para. Archivos ACF, también se usa el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para cargar datos de animación.</span><span class="sxs-lookup"><span data-stu-id="0e983-127">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="0e983-128">El método **Load** no admite la descarga. Archivos de ACS de un sitio HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e983-128">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="0e983-129">Al cargar un carácter, no se muestra automáticamente el carácter.</span><span class="sxs-lookup"><span data-stu-id="0e983-129">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="0e983-130">Use el método [**Show**](show-method.md) primero para que el carácter esté visible.</span><span class="sxs-lookup"><span data-stu-id="0e983-130">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 