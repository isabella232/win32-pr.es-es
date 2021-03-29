---
title: Registro de un archivo DLL de seguridad RAS
description: El programa de instalación de una DLL de seguridad RAS debe registrar el archivo DLL con el servidor RAS de Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775396"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="84497-103">Registro de un archivo DLL de seguridad RAS</span><span class="sxs-lookup"><span data-stu-id="84497-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="84497-104">El programa de instalación de una DLL de seguridad RAS debe registrar el archivo DLL con el servidor RAS de Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="84497-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="84497-105">Solo se puede registrar un archivo DLL de seguridad RAS porque no se proporciona compatibilidad con varios archivos dll de seguridad.</span><span class="sxs-lookup"><span data-stu-id="84497-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="84497-106">Para registrar un archivo DLL de seguridad RAS, establezca el valor *DLLPath* bajo la clave siguiente en el registro:</span><span class="sxs-lookup"><span data-stu-id="84497-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="84497-107">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="84497-107">Value name</span></span> | <span data-ttu-id="84497-108">Datos del valor</span><span class="sxs-lookup"><span data-stu-id="84497-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84497-109">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="84497-109">*DLLPath*</span></span>  | <span data-ttu-id="84497-110">Una cadena **reg \_ SZ** que contiene la ruta de acceso del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="84497-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="84497-111">Esta cadena debe especificar la ruta de acceso completa a menos que el archivo DLL esté en un directorio que aparezca en la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="84497-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="84497-112">El programa de instalación de un archivo DLL de seguridad RAS también debe proporcionar la funcionalidad de quitar o desinstalar.</span><span class="sxs-lookup"><span data-stu-id="84497-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="84497-113">Si un usuario quita el archivo DLL, el programa de instalación debe eliminar el valor *DLLPath* del registro.</span><span class="sxs-lookup"><span data-stu-id="84497-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="84497-114">El servicio RAS no se inicia si el valor *DLLPath* especifica un archivo DLL que no se puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="84497-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="84497-115">Un archivo DLL de seguridad RAS debe exportar las funciones [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) y [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .</span><span class="sxs-lookup"><span data-stu-id="84497-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




