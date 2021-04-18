---
description: Cómo excluir una aplicación del cuadro de diálogo Abrir con para el tipo de archivo no asociado.
title: Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561121"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a><span data-ttu-id="8cb72-103">Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados</span><span class="sxs-lookup"><span data-stu-id="8cb72-103">How to Exclude an Application from the Open With Dialog Box for Unassociated File Types</span></span>

<span data-ttu-id="8cb72-104">Cuando un usuario intenta abrir un archivo que no es miembro de ningún tipo de archivo registrado (es decir, un tipo de archivo desconocido) o cuando un usuario selecciona **abrir con** o **abrir con-> elegir programa predeterminado** en el menú contextual de un archivo, el shell presenta un submenú o un cuadro de diálogo que permite al usuario especificar el programa que se usa para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="8cb72-104">When a user attempts to open a file that is not a member of any registered file type (that is, an unknown file type), or when a user selects **Open with** or **Open with -> Choose default program** from a file's shortcut menu, the Shell presents a submenu or dialog box that enables the user to specify the program used to open the file.</span></span>

<span data-ttu-id="8cb72-105">De forma predeterminada, todas las aplicaciones registradas como subclaves de las aplicaciones **\_ \_ raíz de clases HKEY** \\  se presentan en el cuadro de diálogo **abrir con** .</span><span class="sxs-lookup"><span data-stu-id="8cb72-105">By default, any application registered as a subkey of **HKEY\_CLASSES\_ROOT**\\**Applications** is presented in the **Open with** dialog box.</span></span> <span data-ttu-id="8cb72-106">Estas aplicaciones se presentan en **abierto con** independencia de si la aplicación está registrada para controlar el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8cb72-106">These applications are presented in **Open with** regardless of whether the application is registered to handle the file type.</span></span>

<span data-ttu-id="8cb72-107">Para evitar que una aplicación aparezca en el cuadro de diálogo **abrir con** cuando la aplicación no debe o no se puede usar para abrir determinados tipos de archivo, utilice una de las dos técnicas descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="8cb72-107">To prevent an application from appearing in the **Open with** dialog box when the application should not or cannot be used to open certain file types, use one of the two techniques described in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="8cb72-108">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="8cb72-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8cb72-109">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="8cb72-109">Step 1:</span></span>

<span data-ttu-id="8cb72-110">Agregue una entrada NoOpenWith a la subclave de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cb72-110">Add a NoOpenWith entry to the application's subkey.</span></span> <span data-ttu-id="8cb72-111">Cuando una aplicación utiliza un tipo de archivo, Windows registra esa información para generar la lista de **Programas recomendados** .</span><span class="sxs-lookup"><span data-stu-id="8cb72-111">When an application uses a file type, Windows records that information to build the **Recommended Programs** list.</span></span> <span data-ttu-id="8cb72-112">Esta lista se presenta en el submenú **abrir con** , como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8cb72-112">This list is presented in the **Open with** submenu as shown in the following screen shot.</span></span>

![captura de pantalla del menú contextual con el submenú abrir con mostrado](images/file-assoc/openwithsubmenu.png)

<span data-ttu-id="8cb72-114">Estas aplicaciones recomendadas también se muestran en la parte **Programas recomendados** del cuadro de diálogo **abrir con** , como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8cb72-114">These recommended applications are also shown in the **Recommended Programs** portion of the **Open with** dialog box as shown in the following screen shot.</span></span>

![captura de pantalla del cuadro de diálogo Abrir con con los programas recomendados](images/file-assoc/openwithdialog.png)

> [!Note]  
> <span data-ttu-id="8cb72-116">Si una aplicación se ha registrado en [OpenWithList](fa-file-types.md) o OpenWithProgIDs para el tipo de archivo, aparecerá en la lista de **Programas recomendados** aunque se establezca la entrada NoOpenWith.</span><span class="sxs-lookup"><span data-stu-id="8cb72-116">If an application has registered itself in the [OpenWithList](fa-file-types.md) or OpenWithProgIDs for the file type, it will appear in the **Recommended Programs** list even if the NoOpenWith entry is set.</span></span> <span data-ttu-id="8cb72-117">Además, recuerde que, independientemente de si una aplicación se ofrece en una lista de programas recomendados, un usuario puede examinar manualmente cualquier archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="8cb72-117">Also, remember that regardless of whether an application is offered in a list of recommended programs, a user can manually browse to any executable file.</span></span>

 

<span data-ttu-id="8cb72-118">Las aplicaciones pueden deshabilitar este seguimiento especificando un valor de NoOpenWith en la subclave de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cb72-118">Applications can disable this tracking by specifying a NoOpenWith value under the application's subkey.</span></span>

<span data-ttu-id="8cb72-119">La entrada NoOpenWith es un valor **reg \_ SZ** vacío tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8cb72-119">The NoOpenWith entry is an empty **REG\_SZ** value as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

<span data-ttu-id="8cb72-120">La configuración de la entrada NoOpenWith también tiene estos efectos:</span><span class="sxs-lookup"><span data-stu-id="8cb72-120">Setting the NoOpenWith entry also has these effects:</span></span>

-   <span data-ttu-id="8cb72-121">Impide anclar un archivo a la Jump List de la aplicación a través de la función de arrastrar y colocar, a menos que la aplicación se registre específicamente para controlar ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8cb72-121">Prevents pinning a file to the application's Jump List through drag-and-drop, unless the application is specifically registered to handle that file type.</span></span>
-   <span data-ttu-id="8cb72-122">Impide que el cuadro de diálogo archivo común y las llamadas a la función [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) agreguen cualquier archivo a la Jump List de la aplicación, a menos que la aplicación se registre específicamente para administrar ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8cb72-122">Prevents the common file dialog box and any call to the [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) function from adding any file to the application's Jump List, unless the application is specifically registered to handle that file type.</span></span>

### <a name="step-2"></a><span data-ttu-id="8cb72-123">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="8cb72-123">Step 2:</span></span>

<span data-ttu-id="8cb72-124">La segunda manera de impedir que una aplicación aparezca en el cuadro de diálogo **abrir con** es usar la subclave **SupportedTypes** para enumerar explícitamente las extensiones de los tipos de archivo que la aplicación puede abrir.</span><span class="sxs-lookup"><span data-stu-id="8cb72-124">The second way to prevent an application from appearing in the **Open with** dialog box is to use the **SupportedTypes** subkey to explicitly list the extensions of file types that the application can open.</span></span> <span data-ttu-id="8cb72-125">Esto evita que la aplicación aparezca en el cuadro de diálogo **abrir con** para los tipos de archivo que no se pueden abrir.</span><span class="sxs-lookup"><span data-stu-id="8cb72-125">This prevents the application from appearing in the **Open with** dialog box for file types that it cannot open.</span></span> <span data-ttu-id="8cb72-126">También hace que la aplicación aparezca en la lista de **Programas recomendados** , tal como se explicó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8cb72-126">It also causes the application to appear in the **Recommended Programs** list as discussed previously.</span></span>

<span data-ttu-id="8cb72-127">Este método es especialmente útil si una aplicación puede guardar un archivo como un tipo de archivo determinado pero no puede abrir ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8cb72-127">This method is particularly useful if an application can save a file as a certain file type but cannot open that file type.</span></span> <span data-ttu-id="8cb72-128">Una aplicación también debe establecer la marca de FOS \_ DONTADDTORECENT a través de [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) al llamar al cuadro de diálogo **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="8cb72-128">An application should also set the FOS\_DONTADDTORECENT flag through [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) when calling the **Save** dialog box.</span></span> <span data-ttu-id="8cb72-129">Esto evita que se agregue el elemento a las partes **recientes** o **frecuentes** de una Jump List.</span><span class="sxs-lookup"><span data-stu-id="8cb72-129">This keeps the item from being added to the **Recent** or **Frequent** portions of a Jump List.</span></span> <span data-ttu-id="8cb72-130">También impide que se realice un seguimiento de la aplicación en [OpenWithList](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="8cb72-130">It also blocks the application from being tracked under [OpenWithList](fa-file-types.md).</span></span>

<span data-ttu-id="8cb72-131">Cada extensión admitida se agrega como una entrada en la subclave **SupportedTypes** , tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8cb72-131">Each supported extension is added as an entry under the **SupportedTypes** subkey as shown in the following example.</span></span> <span data-ttu-id="8cb72-132">Las entradas son del tipo **reg \_ SZ** o **reg \_ null**, sin valores asociados.</span><span class="sxs-lookup"><span data-stu-id="8cb72-132">The entries are of type **REG\_SZ** or **REG\_NULL**, with no associated values.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

<span data-ttu-id="8cb72-133">Si se proporciona una subclave **SupportedTypes** , solo los archivos con esas extensiones son válidos para el anclaje a la Jump List de la aplicación o para que se realice el seguimiento en la lista de destinos **recientes** o **frecuentes** de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cb72-133">If a **SupportedTypes** subkey is provided, only files with those extensions are eligible for pinning to the application's Jump List or for being tracked in an application's **Recent** or **Frequent** destinations list.</span></span>

<span data-ttu-id="8cb72-134">La entrada NoOpenWith invalida la subclave **SupportedTypes** y oculta la aplicación en el cuadro de diálogo **abrir con** .</span><span class="sxs-lookup"><span data-stu-id="8cb72-134">The NoOpenWith entry overrides the **SupportedTypes** subkey and hides the application in the **Open with** dialog box.</span></span>

 

 
