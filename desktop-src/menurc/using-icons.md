---
title: Usar iconos
description: En esta sección se proporcionan ejemplos de código que muestran cómo realizar tareas relacionadas con iconos.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- recursos, iconos
- iconos, crear
- iconos, Mostrar
- iconos, compartir recursos
- crear iconos
- mostrar iconos
- compartir recursos de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e93f831e3411985ecfb9f841ade750acd4a61b
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2021
ms.locfileid: "105661417"
---
# <a name="using-icons"></a><span data-ttu-id="9e608-110">Usar iconos</span><span class="sxs-lookup"><span data-stu-id="9e608-110">Using Icons</span></span>

<span data-ttu-id="9e608-111">En los temas siguientes se describe cómo realizar ciertas tareas relacionadas con los iconos:</span><span class="sxs-lookup"><span data-stu-id="9e608-111">The following topics describe how to perform certain tasks related to icons:</span></span>

-   [<span data-ttu-id="9e608-112">Crear un icono</span><span class="sxs-lookup"><span data-stu-id="9e608-112">Creating an Icon</span></span>](#creating-an-icon)
-   [<span data-ttu-id="9e608-113">Mostrar un icono</span><span class="sxs-lookup"><span data-stu-id="9e608-113">Displaying an Icon</span></span>](#displaying-an-icon)
-   [<span data-ttu-id="9e608-114">Compartir recursos de icono</span><span class="sxs-lookup"><span data-stu-id="9e608-114">Sharing Icon Resources</span></span>](#sharing-icon-resources)

## <a name="creating-an-icon"></a><span data-ttu-id="9e608-115">Crear un icono</span><span class="sxs-lookup"><span data-stu-id="9e608-115">Creating an Icon</span></span>

<span data-ttu-id="9e608-116">Para usar un icono, la aplicación debe obtener un identificador para el icono.</span><span class="sxs-lookup"><span data-stu-id="9e608-116">To use an icon, your application must get a handle to the icon.</span></span> <span data-ttu-id="9e608-117">En el ejemplo siguiente se muestra cómo crear dos identificadores de icono diferentes: uno para el icono de pregunta estándar y otro para un icono personalizado incluido como un recurso en el archivo de definición de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e608-117">The following example shows how to create two different icon handles: one for the standard question icon and one for a custom icon included as a resource in the application's resource-definition file.</span></span>


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



<span data-ttu-id="9e608-118">Una aplicación debe implementar iconos personalizados como recursos y debe utilizar la función [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) , en lugar de crear los iconos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9e608-118">An application should implement custom icons as resources and should use the [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function, rather than create the icons at run-time.</span></span> <span data-ttu-id="9e608-119">Este enfoque evita la dependencia del dispositivo, simplifica la localización y permite que las aplicaciones compartan los mapas de bits de los iconos.</span><span class="sxs-lookup"><span data-stu-id="9e608-119">This approach avoids device dependence, simplifies localization, and enables applications to share icon bitmaps.</span></span> <span data-ttu-id="9e608-120">Sin embargo, en el ejemplo siguiente se usa [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) para crear un icono personalizado en tiempo de ejecución, basado en máscaras de bits de mapa de bits. se incluye para mostrar cómo interpreta el sistema las máscaras de bits de los mapas de bits de los iconos.</span><span class="sxs-lookup"><span data-stu-id="9e608-120">However, the following example uses [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) to create a custom icon at run-time, based on bitmap bitmasks; it is included to illustrate how the system interprets icon bitmap bitmasks.</span></span>


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



<span data-ttu-id="9e608-121">Para crear el icono, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) aplica la siguiente tabla de verdad a las máscaras de máscara y y XOR.</span><span class="sxs-lookup"><span data-stu-id="9e608-121">To create the icon, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applies the following truth table to the AND and XOR bitmasks.</span></span>



| <span data-ttu-id="9e608-122">Y máscara de la</span><span class="sxs-lookup"><span data-stu-id="9e608-122">AND bitmask</span></span> | <span data-ttu-id="9e608-123">Máscara de máscara XOR</span><span class="sxs-lookup"><span data-stu-id="9e608-123">XOR bitmask</span></span> | <span data-ttu-id="9e608-124">Pantalla</span><span class="sxs-lookup"><span data-stu-id="9e608-124">Display</span></span>        |
|-------------|-------------|----------------|
| <span data-ttu-id="9e608-125">0</span><span class="sxs-lookup"><span data-stu-id="9e608-125">0</span></span>           | <span data-ttu-id="9e608-126">0</span><span class="sxs-lookup"><span data-stu-id="9e608-126">0</span></span>           | <span data-ttu-id="9e608-127">Negro</span><span class="sxs-lookup"><span data-stu-id="9e608-127">Black</span></span>          |
| <span data-ttu-id="9e608-128">0</span><span class="sxs-lookup"><span data-stu-id="9e608-128">0</span></span>           | <span data-ttu-id="9e608-129">1</span><span class="sxs-lookup"><span data-stu-id="9e608-129">1</span></span>           | <span data-ttu-id="9e608-130">Blanco</span><span class="sxs-lookup"><span data-stu-id="9e608-130">White</span></span>          |
| <span data-ttu-id="9e608-131">1</span><span class="sxs-lookup"><span data-stu-id="9e608-131">1</span></span>           | <span data-ttu-id="9e608-132">0</span><span class="sxs-lookup"><span data-stu-id="9e608-132">0</span></span>           | <span data-ttu-id="9e608-133">Screen</span><span class="sxs-lookup"><span data-stu-id="9e608-133">Screen</span></span>         |
| <span data-ttu-id="9e608-134">1</span><span class="sxs-lookup"><span data-stu-id="9e608-134">1</span></span>           | <span data-ttu-id="9e608-135">1</span><span class="sxs-lookup"><span data-stu-id="9e608-135">1</span></span>           | <span data-ttu-id="9e608-136">Pantalla invertida</span><span class="sxs-lookup"><span data-stu-id="9e608-136">Reverse screen</span></span> |



 

<span data-ttu-id="9e608-137">Antes de cerrar, la aplicación debe usar [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) para destruir cualquier icono que haya creado con [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span><span class="sxs-lookup"><span data-stu-id="9e608-137">Before closing, your application must use [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) to destroy any icon it created by using [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span></span> <span data-ttu-id="9e608-138">No es necesario destruir iconos creados por otras funciones.</span><span class="sxs-lookup"><span data-stu-id="9e608-138">It is not necessary to destroy icons created by other functions.</span></span>

## <a name="displaying-an-icon"></a><span data-ttu-id="9e608-139">Mostrar un icono</span><span class="sxs-lookup"><span data-stu-id="9e608-139">Displaying an Icon</span></span>

<span data-ttu-id="9e608-140">La aplicación puede cargar y crear iconos para mostrar en el área de cliente o las ventanas secundarias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e608-140">Your application can load and create icons to display in the application's client area or child windows.</span></span> <span data-ttu-id="9e608-141">En el ejemplo siguiente se muestra cómo dibujar un icono en el área cliente de la ventana cuyo contexto de dispositivo (DC) se identifica mediante el parámetro *HDC* .</span><span class="sxs-lookup"><span data-stu-id="9e608-141">The following example demonstrates how to draw an icon in the client area of the window whose device context (DC) is identified by the *hdc* parameter.</span></span>


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



<span data-ttu-id="9e608-142">El sistema muestra automáticamente los iconos de clase de una ventana.</span><span class="sxs-lookup"><span data-stu-id="9e608-142">The system automatically displays the class icon(s) for a window.</span></span> <span data-ttu-id="9e608-143">La aplicación puede asignar iconos de clase al registrar una clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="9e608-143">Your application can assign class icons while registering a window class.</span></span> <span data-ttu-id="9e608-144">La aplicación puede reemplazar un icono de clase mediante la función [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) .</span><span class="sxs-lookup"><span data-stu-id="9e608-144">Your application can replace a class icon by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="9e608-145">Esta función cambia la configuración de ventana predeterminada para todas las ventanas de una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="9e608-145">This function changes the default window settings for all windows of a given class.</span></span> <span data-ttu-id="9e608-146">En el ejemplo siguiente se reemplaza un icono de clase con el icono cuyo identificador de recurso es 480.</span><span class="sxs-lookup"><span data-stu-id="9e608-146">The following example replaces a class icon with the icon whose resource identifier is 480.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLong(hwnd,          // window handle 
    GCL_HICON,              // changes icon 
    (LONG) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



<span data-ttu-id="9e608-147">Para obtener más información sobre las clases de ventana, vea [clases de ventana](/windows/desktop/winmsg/window-classes).</span><span class="sxs-lookup"><span data-stu-id="9e608-147">For more information about window classes, see [Window Classes](/windows/desktop/winmsg/window-classes).</span></span>

## <a name="sharing-icon-resources"></a><span data-ttu-id="9e608-148">Compartir recursos de icono</span><span class="sxs-lookup"><span data-stu-id="9e608-148">Sharing Icon Resources</span></span>

<span data-ttu-id="9e608-149">En el código siguiente se usan las funciones [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)y [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), y algunas de las funciones de recursos, para crear un identificador de icono basado en los datos de icono de otro archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="9e608-149">The following code uses the functions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), and [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), and several of the resource functions, to create an icon handle based on icon data from another executable file.</span></span> <span data-ttu-id="9e608-150">A continuación, muestra el icono en una ventana.</span><span class="sxs-lookup"><span data-stu-id="9e608-150">Then, it displays the icon in a window.</span></span>

<span data-ttu-id="9e608-151">**Advertencia de seguridad:** El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="9e608-151">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="9e608-152">Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9e608-152">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
