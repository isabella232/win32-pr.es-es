---
title: El archivo de registro de la interfaz
description: El archivo de registro de la interfaz recopila información que ayuda en el registro de interfaces COM empaquetadas en un archivo DLL o EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- archivo de registro de interfaz MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665813"
---
# <a name="the-interface-registration-file"></a><span data-ttu-id="09b2d-104">El archivo de registro de la interfaz</span><span class="sxs-lookup"><span data-stu-id="09b2d-104">The Interface Registration File</span></span>

<span data-ttu-id="09b2d-105">El archivo de registro de la interfaz recopila información que ayuda en el registro de interfaces COM empaquetadas en un archivo DLL o EXE.</span><span class="sxs-lookup"><span data-stu-id="09b2d-105">The interface registration file collects information that helps in the registration of COM interfaces packaged into a DLL or EXE file.</span></span> <span data-ttu-id="09b2d-106">El archivo de registro de la interfaz es diferente de otros archivos generados porque puede recopilar información de la compilación de varios archivos IDL diferentes.</span><span class="sxs-lookup"><span data-stu-id="09b2d-106">The interface registration file is different from other generated files because it can gather information from compiling several different IDL files.</span></span> <span data-ttu-id="09b2d-107">Cada ejecución del compilador de MIDL para interfaces COM busca primero un archivo dlldata. c existente y, si no se encuentra el archivo, se crea un nuevo archivo dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="09b2d-107">Each MIDL compiler run for COM interfaces looks for an existing dlldata.c file first, and if the file is not found, a new dlldata.c file is created.</span></span> <span data-ttu-id="09b2d-108">Si se encuentra un archivo dlldata. c, se agrega información sobre el IDL actual (si no existe) o se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="09b2d-108">If a dlldata.c file is found, information about the current IDL is added (if absent) or replaced.</span></span>

<span data-ttu-id="09b2d-109">El archivo de registro de la interfaz se genera o actualiza de forma segura en un entorno con varios procesadores porque las compilaciones MIDL paralelas no pueden escribir en el archivo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="09b2d-109">The interface registration file is safely generated or updated in a multiprocessor environment because parallel MIDL compiles are prevented from writing to the file at the same time.</span></span> <span data-ttu-id="09b2d-110">Dado que cualquier archivo dlldata. c puede marcarse como de solo lectura en el entorno de compilación o el usuario, el compilador MIDL implementa un enfoque de tiempo de espera para esperar en un archivo que no se puede abrir y emite un mensaje de error adecuado si el tiempo de espera expira.</span><span class="sxs-lookup"><span data-stu-id="09b2d-110">Because any dlldata.c file can be marked as read-only by either the build environment or the user, the MIDL compiler implements a timeout approach to waiting on a file it cannot open, and issues an appropriate error message if the timeout expires.</span></span>

<span data-ttu-id="09b2d-111">El nombre predeterminado del archivo de registro de la interfaz generado a partir de un archivo de entrada es dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="09b2d-111">The default name for the interface registration file generated from an input file is dlldata.c.</span></span> <span data-ttu-id="09b2d-112">El modificador de compilador MIDL [**/dlldata**](-dlldata.md) se puede usar para reemplazar el nombre predeterminado del archivo.</span><span class="sxs-lookup"><span data-stu-id="09b2d-112">The [**/dlldata**](-dlldata.md) MIDL compiler switch can be used to override the default name of the file.</span></span> <span data-ttu-id="09b2d-113">Reemplazar el nombre predeterminado del archivo de registro de la interfaz es especialmente útil cuando algunos archivos IDL empaquetados en un binario común residen en directorios diferentes.</span><span class="sxs-lookup"><span data-stu-id="09b2d-113">Overriding the default name of the interface registration file is especially useful when some IDL files packaged to a common binary reside in different directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09b2d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09b2d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b2d-115">Compilar y registrar un archivo DLL de proxy</span><span class="sxs-lookup"><span data-stu-id="09b2d-115">Building and Registering a Proxy DLL</span></span>](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 