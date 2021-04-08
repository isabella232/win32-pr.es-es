---
title: Acerca de la configuración del registro del archivo DLL de administración RAS
description: El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RRAS de administración de RAS, configuración del registro de DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103904314"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="d4776-104">Acerca de la configuración del registro del archivo DLL de administración RAS</span><span class="sxs-lookup"><span data-stu-id="d4776-104">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="d4776-105">El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="d4776-105">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d4776-106">Para registrar el archivo DLL, establezca los siguientes valores bajo esta clave.</span><span class="sxs-lookup"><span data-stu-id="d4776-106">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="d4776-107">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="d4776-107">Value name</span></span>    | <span data-ttu-id="d4776-108">Datos del valor</span><span class="sxs-lookup"><span data-stu-id="d4776-108">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d4776-109">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="d4776-109">*DisplayName*</span></span> | <span data-ttu-id="d4776-110">Una cadena **reg \_ SZ** que contiene el nombre descriptivo para mostrar del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d4776-110">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="d4776-111">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="d4776-111">*DLLPath*</span></span>     | <span data-ttu-id="d4776-112">Una cadena **reg \_ SZ** que contiene la ruta de acceso completa del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d4776-112">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="d4776-113">Como RAS admite varios archivos dll de administración de RAS, el valor de registro **DLLPath** puede contener una lista delimitada por punto y coma de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="d4776-113">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="d4776-114">Por ejemplo, la entrada del registro para un archivo DLL de administración de RAS de una compañía ficticia denominada proelectrones, Inc. podría ser la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4776-114">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d4776-115">*DisplayName*: **reg \_ SZ** : dll de administrador de ras de proelectrones</span><span class="sxs-lookup"><span data-stu-id="d4776-115">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="d4776-116">*DLLPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="d4776-116">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="d4776-117">RAS llama a los archivos dll en el orden en que aparecen en este valor del registro.</span><span class="sxs-lookup"><span data-stu-id="d4776-117">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="d4776-118">El valor de *displayName* del valor del registro todavía contiene un solo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="d4776-118">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="d4776-119">El programa de instalación de una DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación y desinstalación.</span><span class="sxs-lookup"><span data-stu-id="d4776-119">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="d4776-120">Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del registro para el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="d4776-120">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="d4776-121">**Windows 2000/NT:** RAS solo admite un archivo DLL de administración RAS, por lo que el valor de registro **DLLPath** no puede contener una lista de rutas de acceso delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="d4776-121">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




