---
title: Configuración del registro del archivo DLL de administración de RAS
description: El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532409"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="a14cc-103">Configuración del registro del archivo DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="a14cc-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="a14cc-104">El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="a14cc-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="a14cc-105">Para registrar el archivo DLL, establezca los siguientes valores bajo esta clave.</span><span class="sxs-lookup"><span data-stu-id="a14cc-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="a14cc-106">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="a14cc-106">Value name</span></span>    | <span data-ttu-id="a14cc-107">Datos del valor</span><span class="sxs-lookup"><span data-stu-id="a14cc-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a14cc-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="a14cc-108">*DisplayName*</span></span> | <span data-ttu-id="a14cc-109">Una cadena **reg \_ SZ** que contiene el nombre descriptivo para mostrar del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="a14cc-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="a14cc-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="a14cc-110">*DLLPath*</span></span>     | <span data-ttu-id="a14cc-111">Una cadena **reg \_ SZ** que contiene la ruta de acceso completa del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="a14cc-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="a14cc-112">Por ejemplo, la entrada del registro para un archivo DLL de administración de RAS de una compañía ficticia denominada proelectrones, Inc. podría ser:</span><span class="sxs-lookup"><span data-stu-id="a14cc-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="a14cc-113">*DisplayName* : **reg \_ SZ** : dll de administrador de ras de proelectrones</span><span class="sxs-lookup"><span data-stu-id="a14cc-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="a14cc-114">*DLLPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="a14cc-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="a14cc-115">El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de quitar o desinstalar.</span><span class="sxs-lookup"><span data-stu-id="a14cc-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="a14cc-116">Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del registro del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="a14cc-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




