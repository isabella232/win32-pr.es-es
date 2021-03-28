---
description: Se debe asignar un icono personalizado a un tipo de archivo para proporcionar una indicación visual al usuario de ese tipo de archivo o a la aplicación a la que está asociado el tipo de archivo.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Cómo asignar un icono personalizado a un tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985470"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="6ff2d-103">Cómo asignar un icono personalizado a un tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="6ff2d-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="6ff2d-104">Cuando no se asigna ningún icono predeterminado personalizado a un tipo de archivo, el escritorio y el explorador de Windows muestran todos los archivos de ese tipo con un icono predeterminado genérico.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="6ff2d-105">Por ejemplo, en la siguiente captura de pantalla se muestra este icono predeterminado que se usa con el archivo MyDocs4. MYP.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![captura de pantalla del icono predeterminado](images/icon.png)

<span data-ttu-id="6ff2d-107">Aunque todos los archivos que se muestran en esta captura de pantalla son archivos de texto simples, solo MyDocs4. MYP muestra el icono predeterminado de Windows.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="6ff2d-108">Esto se debe a que la extensión. txt es un tipo de archivo registrado que tiene un icono predeterminado personalizado.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="6ff2d-109">En la captura de pantalla siguiente se muestra un icono personalizado que se ha asignado al tipo de archivo. MYP.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![captura de pantalla del icono personalizado para los archivos. MYP](images/context4.png)

> [!Note]  
> <span data-ttu-id="6ff2d-111">Los iconos también se pueden asignar de acuerdo con una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="6ff2d-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="6ff2d-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="6ff2d-113">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="6ff2d-113">Step 1:</span></span>

<span data-ttu-id="6ff2d-114">Cree una subclave denominada **DefaultIcon** en una de las dos ubicaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="6ff2d-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="6ff2d-115">Para una asignación de tipo de archivo **, \_ clases HKEY \_ raíz** \\ *. Extension*</span><span class="sxs-lookup"><span data-stu-id="6ff2d-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="6ff2d-116">Para una asignación de aplicación **, \_ clases HKEY \_ raíz** \\ *ProgID*</span><span class="sxs-lookup"><span data-stu-id="6ff2d-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="6ff2d-117">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="6ff2d-117">Step 2:</span></span>

<span data-ttu-id="6ff2d-118">Asigne a la subclave **DefaultIcon** un valor predeterminado de tipo **reg \_ SZ** que especifique la ruta de acceso completa del archivo que contiene el icono.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="6ff2d-119">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="6ff2d-119">Step 3:</span></span>

<span data-ttu-id="6ff2d-120">Llame a la función [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar al shell que actualice su caché de iconos.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff2d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ff2d-121">Remarks</span></span>

<span data-ttu-id="6ff2d-122">En el ejemplo siguiente se muestra una vista detallada de las entradas del registro necesarias para una asignación de icono de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="6ff2d-123">La extensión de nombre de archivo está asociada a una aplicación, pero la asignación de icono es a la propia extensión de nombre de archivo, por lo que la aplicación asociada no dicta el icono predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="6ff2d-124">En el ejemplo siguiente se muestra una vista detallada de las entradas del registro necesarias para la asignación de un icono de aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="6ff2d-125">La extensión de nombre de archivo. MYP se asocia primero a la aplicación de mi programa. 1.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="6ff2d-126">A continuación, se asigna a la subclave de PROG. 1 ProgID el icono predeterminado personalizado.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="6ff2d-127">Cualquier archivo que contenga un icono es aceptable, incluidos los archivos. ico,. exe y. dll.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="6ff2d-128">Si hay más de un icono en el archivo, la ruta de acceso debe ir seguida de una coma y, a continuación, el índice del icono.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ff2d-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ff2d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ff2d-130">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="6ff2d-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



