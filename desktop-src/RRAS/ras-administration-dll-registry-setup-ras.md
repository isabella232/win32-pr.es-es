---
title: Instalación del Registro DLL de administración de RAS
description: Comprenda los requisitos para registrar un archivo DLL de administración del servicio de acceso remoto (RAS) de terceros con RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406718"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="c4b62-103">Instalación del Registro DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="c4b62-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="c4b62-104">El programa de instalación de un archivo DLL de administración de RAS de terceros debe registrar el archivo DLL con RAS proporcionando información con la siguiente clave en el Registro.</span><span class="sxs-lookup"><span data-stu-id="c4b62-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="c4b62-105">Para registrar el archivo DLL, establezca los siguientes valores en esta clave.</span><span class="sxs-lookup"><span data-stu-id="c4b62-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="c4b62-106">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="c4b62-106">Value name</span></span>    | <span data-ttu-id="c4b62-107">Datos del valor</span><span class="sxs-lookup"><span data-stu-id="c4b62-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="c4b62-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="c4b62-108">*DisplayName*</span></span> | <span data-ttu-id="c4b62-109">Cadena **REG \_ SZ** que contiene el nombre para mostrar descriptivo del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c4b62-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="c4b62-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="c4b62-110">*DLLPath*</span></span>     | <span data-ttu-id="c4b62-111">Cadena **REG \_ SZ** que contiene la ruta de acceso completa del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c4b62-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="c4b62-112">Por ejemplo, la entrada del Registro para un archivo DLL de administración de RAS de una empresa ficticia denominada ProElectrón, Inc. podría ser:</span><span class="sxs-lookup"><span data-stu-id="c4b62-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="c4b62-113">*DisplayName* : **REG \_ SZ** : DLL de administración de RAS de ProElectrón</span><span class="sxs-lookup"><span data-stu-id="c4b62-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="c4b62-114">*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="c4b62-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="c4b62-115">El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="c4b62-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="c4b62-116">Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del Registro del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c4b62-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




