---
description: En Windows 7 y versiones posteriores, puede Agregar verbos a una carpeta mediante Desktop.ini. Para obtener más información acerca de los archivos de Desktop.ini, consulte Cómo personalizar carpetas con Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Cómo implementar verbos personalizados para carpetas a través de Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985434"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="05545-104">Cómo implementar verbos personalizados para carpetas a través de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="05545-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="05545-105">En Windows 7 y versiones posteriores, puede Agregar verbos a una carpeta mediante Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="05545-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="05545-106">Para obtener más información acerca de los archivos de Desktop.ini, consulte [Cómo personalizar carpetas con Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="05545-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="05545-107">Desktop.ini archivos siempre deben estar marcados como **sistema**  +  **oculto** para que no se muestren a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="05545-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="05545-108">Para agregar verbos personalizados para carpetas a través de un archivo de Desktop.ini, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="05545-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="05545-109">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="05545-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="05545-110">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="05545-110">Step 1:</span></span>

<span data-ttu-id="05545-111">Cree una carpeta marcada como **de solo lectura** o **sistema**.</span><span class="sxs-lookup"><span data-stu-id="05545-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="05545-112">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="05545-112">Step 2:</span></span>

<span data-ttu-id="05545-113">Cree un archivo de Desktop.ini que incluya un \[ . ShellClassInfo \] DirectoryClass = ProgID.</span><span class="sxs-lookup"><span data-stu-id="05545-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="05545-114">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="05545-114">Step 3:</span></span>

<span data-ttu-id="05545-115">En el registro, cree la carpeta **\_ \_ raíz de las clases HKEY** \\  con un valor de CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="05545-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="05545-116">El valor CanUseForDirectory evita el uso incorrecto de los ProgID que se establecen para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="05545-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="05545-117">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="05545-117">Step 4:</span></span>

<span data-ttu-id="05545-118">Agregue verbos en la subclave ProgID de la **carpeta** , por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="05545-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="05545-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05545-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05545-120">Estos verbos pueden ser los verbos predeterminados, en cuyo caso, al hacer doble clic en la carpeta, se activa el verbo.</span><span class="sxs-lookup"><span data-stu-id="05545-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



