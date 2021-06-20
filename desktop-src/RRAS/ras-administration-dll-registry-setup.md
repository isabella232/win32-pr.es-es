---
title: Acerca de la instalación del Registro DLL de administración de RAS
description: Comprenda los requisitos para registrar un archivo DLL de administración del servicio de acceso remoto (RAS) de terceros con RAS. RAS admite varios archivos DLL de administración de RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS Administration RRAS , dll registry setup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406668"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="51a36-105">Acerca de la instalación del Registro DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="51a36-105">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="51a36-106">El programa de instalación de un archivo DLL de administración de RAS de terceros debe registrar el archivo DLL con RAS proporcionando información con la siguiente clave en el Registro.</span><span class="sxs-lookup"><span data-stu-id="51a36-106">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="51a36-107">Para registrar el archivo DLL, establezca los siguientes valores en esta clave.</span><span class="sxs-lookup"><span data-stu-id="51a36-107">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="51a36-108">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="51a36-108">Value name</span></span>    | <span data-ttu-id="51a36-109">Datos del valor</span><span class="sxs-lookup"><span data-stu-id="51a36-109">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="51a36-110">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="51a36-110">*DisplayName*</span></span> | <span data-ttu-id="51a36-111">Cadena **REG \_ SZ** que contiene el nombre para mostrar descriptivo del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="51a36-111">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="51a36-112">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="51a36-112">*DLLPath*</span></span>     | <span data-ttu-id="51a36-113">Cadena **REG \_ SZ** que contiene la ruta de acceso completa del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="51a36-113">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="51a36-114">Dado que RAS admite varios archivos DLL de administración de RAS, el valor del Registro **DLLPath** puede contener una lista delimitada por punto y coma de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="51a36-114">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="51a36-115">Por ejemplo, la entrada del Registro para un archivo DLL de administración de RAS de una empresa ficticia denominada ProElectrón, Inc., podría ser la siguiente:</span><span class="sxs-lookup"><span data-stu-id="51a36-115">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="51a36-116">*DisplayName*: **REG \_ SZ** : DLL de administración de RAS de ProElectrón</span><span class="sxs-lookup"><span data-stu-id="51a36-116">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="51a36-117">*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="51a36-117">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="51a36-118">RAS llama a los archivos DLL en el orden en que aparecen en este valor del Registro.</span><span class="sxs-lookup"><span data-stu-id="51a36-118">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="51a36-119">El valor del Registro *DisplayName* todavía contiene solo un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="51a36-119">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="51a36-120">El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación y desinstalación.</span><span class="sxs-lookup"><span data-stu-id="51a36-120">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="51a36-121">Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del Registro para el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="51a36-121">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="51a36-122">**Windows 2000/NT:** RAS solo admite un archivo DLL de administración de RAS, por lo que el valor del Registro **DLLPath** no puede contener una lista delimitada por punto y coma de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="51a36-122">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




