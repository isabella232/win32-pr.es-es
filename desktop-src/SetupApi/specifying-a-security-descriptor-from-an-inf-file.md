---
description: Puede controlar la capacidad de un proceso para tener acceso a objetos protegibles o para realizar tareas de administración del sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Especificación de un descriptor de seguridad de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002962"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="f114b-103">Especificación de un descriptor de seguridad de un archivo INF</span><span class="sxs-lookup"><span data-stu-id="f114b-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="f114b-104">Puede controlar la capacidad de un proceso para tener acceso a objetos protegibles o para realizar tareas de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="f114b-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="f114b-105">Un objeto protegible es un objeto que puede tener un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f114b-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="f114b-106">Todos los objetos con nombre son protegibles.</span><span class="sxs-lookup"><span data-stu-id="f114b-106">All named objects are securable.</span></span> <span data-ttu-id="f114b-107">Algunos objetos sin nombre, como los objetos de proceso y de subprocesos, también pueden tener descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f114b-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="f114b-108">Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="f114b-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="f114b-109">Los [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors) contienen la información de seguridad asociada a los objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="f114b-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="f114b-110">Para la mayoría de los objetos protegibles, puede especificar el descriptor de seguridad de un objeto en la llamada de función que crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="f114b-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="f114b-111">Por ejemplo, puede especificar un descriptor de seguridad en las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="f114b-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="f114b-112">Para establecer un descriptor de seguridad a partir de un archivo INF, agregue una sección de seguridad creada por el archivo INF-Writer inmediatamente después de la sección que instala el archivo, la clave del registro o el componente.</span><span class="sxs-lookup"><span data-stu-id="f114b-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="f114b-113">La sección de seguridad debe contener una línea con el descriptor de seguridad de cadena escrito en ella con el formato de las [cadenas de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-strings).</span><span class="sxs-lookup"><span data-stu-id="f114b-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="f114b-114">La línea también debe incluirse entre comillas (").</span><span class="sxs-lookup"><span data-stu-id="f114b-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="f114b-115">Por ejemplo, el siguiente fragmento de archivo INF crearía una clave del registro a la que solo los administradores y el sistema tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="f114b-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="f114b-116">Tenga en cuenta que este ejemplo requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="f114b-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="f114b-117">En este caso, el significado de la cadena es que los administradores tienen control total, el sistema tiene control total y el acceso se puede heredar en todas las subclaves.</span><span class="sxs-lookup"><span data-stu-id="f114b-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="f114b-118">Para obtener más información, consulte [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="f114b-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 
