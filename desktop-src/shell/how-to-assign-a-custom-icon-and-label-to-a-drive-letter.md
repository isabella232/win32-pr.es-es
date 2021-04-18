---
description: Especifique un icono y una etiqueta personalizados para una unidad.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Asignar un icono y una etiqueta personalizados a una letra de unidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985475"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="a6f46-103">Cómo asignar un icono personalizado y una etiqueta a una letra de unidad</span><span class="sxs-lookup"><span data-stu-id="a6f46-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="a6f46-104">Especifique un icono y una etiqueta personalizados para una unidad.</span><span class="sxs-lookup"><span data-stu-id="a6f46-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="a6f46-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a6f46-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="a6f46-106">Paso 1: reemplazar el icono de la unidad estándar por un icono personalizado en Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a6f46-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="a6f46-107">Para reemplazar el icono de la unidad estándar por un icono personalizado en Windows 2000, agregue una subclave denominada para la letra de unidad a la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="a6f46-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="a6f46-108">En el ejemplo siguiente se especifica un icono personalizado y una etiqueta para la unidad E:.</span><span class="sxs-lookup"><span data-stu-id="a6f46-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="a6f46-109">El icono se encuentra en el archivo C: \\ MyDir \\MyDrive.exe con un índice de base cero de tres.</span><span class="sxs-lookup"><span data-stu-id="a6f46-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="a6f46-110">Para Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="a6f46-110">For Windows 2000:</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="a6f46-111">Paso 2: reemplazar el icono de la unidad estándar por un icono personalizado en todas las demás versiones de Windows</span><span class="sxs-lookup"><span data-stu-id="a6f46-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="a6f46-112">Para reemplazar el icono de la unidad estándar por un icono personalizado en todas las versiones de Windows distintas de Windows 2000, agregue una subclave denominada para la letra de unidad a la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="a6f46-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="a6f46-113">En el ejemplo siguiente se especifica un icono personalizado y una etiqueta para la unidad E:.</span><span class="sxs-lookup"><span data-stu-id="a6f46-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="a6f46-114">El icono se encuentra en el archivo C: \\ MyDir \\MyDrive.exe con un índice de base cero de tres.</span><span class="sxs-lookup"><span data-stu-id="a6f46-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="a6f46-115">Para todas las demás versiones de Windows:</span><span class="sxs-lookup"><span data-stu-id="a6f46-115">For all other versions of Windows:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="a6f46-116">Paso 3: llamar al evento SHUpdateImage</span><span class="sxs-lookup"><span data-stu-id="a6f46-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="a6f46-117">En todas las versiones de Windows, si cambia un tipo de archivo o un icono de unidad, también debe llamar a SHUpdateImage para notificar al shell que actualice los iconos que se muestran actualmente.</span><span class="sxs-lookup"><span data-stu-id="a6f46-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f46-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6f46-118">Remarks</span></span>

<span data-ttu-id="a6f46-119">La letra de unidad no debe ir seguida de dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="a6f46-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="a6f46-120">Agregue una subclave **DefaultIcon** a la subclave de la letra de unidad y establezca su valor predeterminado en una cadena que contenga la ubicación del icono.</span><span class="sxs-lookup"><span data-stu-id="a6f46-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="a6f46-121">La primera parte de la cadena contiene la ruta de acceso completa del archivo del icono.</span><span class="sxs-lookup"><span data-stu-id="a6f46-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="a6f46-122">Si hay más de un icono en el archivo, la ruta de acceso va seguida de una coma y, a continuación, el índice de base cero del icono.</span><span class="sxs-lookup"><span data-stu-id="a6f46-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



