---
description: Todas las funciones, prototipos, estructuras y constantes se definen en el archivo de encabezado Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Compilar y probar un archivo DLL de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362008"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="2d7a2-103">Compilar y probar un archivo DLL de GINA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="2d7a2-104">Todas las funciones, prototipos, estructuras y constantes se definen en el archivo de encabezado Winwlx. h.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="2d7a2-105">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="2d7a2-106">Para probar un archivo dll de [*Gina*](/windows/desktop/SecGloss/g-gly) , use el Winlogon.exe de una versión comprobada del sistema operativo, que está disponible en el kit de desarrollo de controladores de Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="2d7a2-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="2d7a2-107">La versión comprobada de [*Winlogon*](/windows/desktop/SecGloss/w-gly) admite la depuración de Gina de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2d7a2-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="2d7a2-108">Puede usar la siguiente sintaxis para crear una sección en Win.ini para especificar las opciones de depuración de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="2d7a2-109">Si se especifica, **logfile** debe contener el nombre completo del archivo que se utilizará para registrar la información de depuración.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="2d7a2-110">Si el archivo no existe, se creará.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="2d7a2-111">Las opciones **DebugFlags** especifican los tipos de información de depuración que se van a escribir en el archivo de registro o el depurador.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="2d7a2-112">**DebugFlags** puede contener una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="2d7a2-113">Marca de depuración</span><span class="sxs-lookup"><span data-stu-id="2d7a2-113">Debugging flag</span></span> | <span data-ttu-id="2d7a2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d7a2-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2d7a2-115">CoolSwitch</span><span class="sxs-lookup"><span data-stu-id="2d7a2-115">CoolSwitch</span></span>     | <span data-ttu-id="2d7a2-116">La combinación de teclas CTRL + ALT + MAYÚS + TAB producirá una interrupción de depuración en Winlogon.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="2d7a2-117">Error</span><span class="sxs-lookup"><span data-stu-id="2d7a2-117">Error</span></span>          | <span data-ttu-id="2d7a2-118">Errores de impresión.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="2d7a2-119">Init</span><span class="sxs-lookup"><span data-stu-id="2d7a2-119">Init</span></span>           | <span data-ttu-id="2d7a2-120">Imprimir mensajes de inicialización y progreso.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="2d7a2-121">Notificar</span><span class="sxs-lookup"><span data-stu-id="2d7a2-121">Notify</span></span>         | <span data-ttu-id="2d7a2-122">Mensajes de paquete de notificación de impresión.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="2d7a2-123">SAS</span><span class="sxs-lookup"><span data-stu-id="2d7a2-123">SAS</span></span>            | <span data-ttu-id="2d7a2-124">Imprime información sobre las notificaciones de [*secuencia de atención segura*](/windows/desktop/SecGloss/s-gly) (SAS).</span><span class="sxs-lookup"><span data-stu-id="2d7a2-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="2d7a2-125">Estado</span><span class="sxs-lookup"><span data-stu-id="2d7a2-125">State</span></span>          | <span data-ttu-id="2d7a2-126">Imprime mensajes cuando Winlogon cambia el estado.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="2d7a2-127">Tiempo de espera</span><span class="sxs-lookup"><span data-stu-id="2d7a2-127">Timeout</span></span>        | <span data-ttu-id="2d7a2-128">Imprime los mensajes cuando se establece un límite de tiempo o se alcanza un límite de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="2d7a2-129">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="2d7a2-129">Trace</span></span>          | <span data-ttu-id="2d7a2-130">Imprime información de seguimiento detallada.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="2d7a2-131">Warn (Advertencia)</span><span class="sxs-lookup"><span data-stu-id="2d7a2-131">Warn</span></span>           | <span data-ttu-id="2d7a2-132">Imprimir advertencias.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="2d7a2-133">Para iniciar la versión comprobada de Winlogon en un depurador, agregue la entrada siguiente al registro:</span><span class="sxs-lookup"><span data-stu-id="2d7a2-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> <span data-ttu-id="2d7a2-134">Debe usar el depurador simbólico de Windows (NTSD) para depurar Winlogon.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d7a2-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d7a2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d7a2-136">Cargar y ejecutar un archivo DLL de GINA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="2d7a2-137">Funciones de exportación de GINA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="2d7a2-138">Estructuras GINA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="2d7a2-139">Terminal Services funciones GINA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
