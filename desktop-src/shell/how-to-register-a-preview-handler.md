---
description: En este tema se explica cómo registrar un controlador de vista previa asociado a un tipo de datos determinado.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Cómo registrar un controlador de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985419"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="e9a1a-103">Cómo registrar un controlador de vista previa</span><span class="sxs-lookup"><span data-stu-id="e9a1a-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="e9a1a-104">En este tema se explica cómo registrar un controlador de vista previa asociado a un tipo de datos determinado.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="e9a1a-105">Para los fines de la ilustración, en los ejemplos de este tema se usa un tipo de archivo. XYZ.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="e9a1a-106">El registro de un controlador de vista previa es un registro estándar basado en asociaciones de archivos.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="e9a1a-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e9a1a-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e9a1a-108">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="e9a1a-108">Step 1:</span></span>

<span data-ttu-id="e9a1a-109">En primer lugar, una extensión de nombre de archivo está asociada a un ProgID.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="e9a1a-110">La entrada siguiente asocia la subclave **xyzfile** ProgID con la extensión de nombre de archivo. XYZ.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="e9a1a-111">La subclave **xyzfile** ProgID se almacena con los otros ProgID, tal como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="e9a1a-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="e9a1a-112">Cada subclave ProgID del controlador de vista previa contiene una subclave denominada **shellex** que contiene una subclave denominada *siempre* **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="e9a1a-113">La presencia de esa subclave indica al sistema que el controlador es un controlador de vista previa.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="e9a1a-114">El valor predeterminado de la subclave **{8895b1c6-b41f-4c1c-a562-0d564250836f}** es el identificador de clase (CLSID) del controlador.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="e9a1a-115">Aquí se muestra un ejemplo de la subclave **xyzfile** ProgID, que asocia un controlador de CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="e9a1a-116">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="e9a1a-116">Step 2:</span></span>

<span data-ttu-id="e9a1a-117">A continuación, agregue la subclave en **CLSID** para el controlador de vista previa.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="e9a1a-118">Aquí se muestra un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-118">An example is shown here.</span></span> <span data-ttu-id="e9a1a-119">A continuación se ofrece una explicación de las entradas individuales.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="e9a1a-120">El valor predeterminado de la subclave (aquí, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) no es necesario ni se usa.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="e9a1a-121">Sin embargo, establecerlo en una cadena no localizada puede ayudarle a depurar problemas de registro.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="e9a1a-122">El signo menos (-101) del recurso. dll de la entrada DisplayName existe por motivos de herencia.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="e9a1a-123">La entrada del icono, por otro lado, no requiere un signo menos.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="e9a1a-124">El valor de AppID proporciona una referencia al AppID de la aplicación asociada a la extensión de nombre de archivo (almacenada en **HKEY \_ clases \_ raíz** \\ **AppID**.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="e9a1a-125">El valor que se usa aquí ({6d2b5079-2f0b-48dd-ab7f-97cec514d30b}) es el identificador del host suplente Prevhost.exe.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="e9a1a-126">los controladores de vista previa de bits de 32 deben usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} cuando se instalan en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="e9a1a-127">Las entradas bajo la subclave **InProcServer32** incluyen una referencia a la subclave ProgID de la extensión de nombre de archivo, así como una entrada para un [VersionIndependentProgID](../com/versionindependentprogid.md).</span><span class="sxs-lookup"><span data-stu-id="e9a1a-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="e9a1a-128">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="e9a1a-128">Step 3:</span></span>

<span data-ttu-id="e9a1a-129">Por último, el controlador de vista previa se debe agregar a la lista de todos los controladores de vista previa.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="e9a1a-130">El sistema usa esta lista como una optimización para enumerar todos los controladores de vista previa registrados con fines de visualización.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="e9a1a-131">De nuevo, el valor predeterminado no es necesario, simplemente contribuye al proceso de depuración.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="e9a1a-132">En Windows 7, si la aplicación está instalada para todos los usuarios del equipo, use HKEY \_ local \_ Machine; si solo hay un usuario, use HKEY \_ Current \_ User.</span><span class="sxs-lookup"><span data-stu-id="e9a1a-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="e9a1a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9a1a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9a1a-134">Controladores de vista previa y host de vista previa de Shell</span><span class="sxs-lookup"><span data-stu-id="e9a1a-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="e9a1a-135">Crear controladores de vista previa</span><span class="sxs-lookup"><span data-stu-id="e9a1a-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="e9a1a-136">Instrucciones de controlador de vista previa</span><span class="sxs-lookup"><span data-stu-id="e9a1a-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
