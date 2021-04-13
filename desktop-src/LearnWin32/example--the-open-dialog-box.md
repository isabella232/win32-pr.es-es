---
title: Ejemplo del cuadro de diálogo abrir
description: El ejemplo de formas que hemos usado es algo inventado. Vamos a convertir un objeto COM que puede usar en un programa de Windows real en el cuadro de diálogo Abrir.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420679"
---
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="76dcd-104">Ejemplo: el cuadro de diálogo abrir</span><span class="sxs-lookup"><span data-stu-id="76dcd-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="76dcd-105">El `Shapes` ejemplo que se ha usado es algo inventado.</span><span class="sxs-lookup"><span data-stu-id="76dcd-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="76dcd-106">Vamos a convertir un objeto COM que puede usar en un programa real de Windows: el cuadro de diálogo **abrir** .</span><span class="sxs-lookup"><span data-stu-id="76dcd-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![captura de pantalla que muestra el cuadro de diálogo abrir](images/fileopen01.png)

<span data-ttu-id="76dcd-108">Para mostrar el cuadro de diálogo **abrir** , un programa puede utilizar un objeto com denominado el objeto de cuadro de diálogo de elementos comunes.</span><span class="sxs-lookup"><span data-stu-id="76dcd-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="76dcd-109">El cuadro de diálogo Common Item implementa una interfaz denominada [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), que se declara en el archivo de encabezado shobjidl. h.</span><span class="sxs-lookup"><span data-stu-id="76dcd-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="76dcd-110">Este es un programa que muestra el cuadro de diálogo **abrir** al usuario.</span><span class="sxs-lookup"><span data-stu-id="76dcd-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="76dcd-111">Si el usuario selecciona un archivo, el programa muestra un cuadro de diálogo que contiene el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="76dcd-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="76dcd-112">Este código usa algunos conceptos que se describirán más adelante en el módulo, por lo que no se preocupe si no comprende todo aquí.</span><span class="sxs-lookup"><span data-stu-id="76dcd-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="76dcd-113">Este es un esquema básico del código:</span><span class="sxs-lookup"><span data-stu-id="76dcd-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="76dcd-114">Llame a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="76dcd-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="76dcd-115">Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto de cuadro de diálogo de elementos comunes y obtener un puntero a la interfaz [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) del objeto.</span><span class="sxs-lookup"><span data-stu-id="76dcd-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="76dcd-116">Llame al método **Show** del objeto, que muestra el cuadro de diálogo al usuario.</span><span class="sxs-lookup"><span data-stu-id="76dcd-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="76dcd-117">Este método se bloquea hasta que el usuario descarta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="76dcd-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="76dcd-118">Llame al método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) del objeto.</span><span class="sxs-lookup"><span data-stu-id="76dcd-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="76dcd-119">Este método devuelve un puntero a un segundo objeto COM, denominado objeto de *elemento de Shell* .</span><span class="sxs-lookup"><span data-stu-id="76dcd-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="76dcd-120">El elemento de Shell, que implementa la interfaz [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , representa el archivo seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="76dcd-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="76dcd-121">Llame al método [**getDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) del elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="76dcd-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="76dcd-122">Este método obtiene la ruta de acceso del archivo, en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="76dcd-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="76dcd-123">Muestra un cuadro de mensaje que muestra la ruta de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="76dcd-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="76dcd-124">Llame a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) para anular la inicialización de la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="76dcd-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="76dcd-125">Los pasos 1, 2 y 7 llaman a las funciones definidas por la biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="76dcd-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="76dcd-126">Se trata de funciones COM genéricas.</span><span class="sxs-lookup"><span data-stu-id="76dcd-126">These are generic COM functions.</span></span> <span data-ttu-id="76dcd-127">Los pasos 3 a 5 llaman a los métodos definidos por el objeto de cuadro de diálogo de elementos comunes.</span><span class="sxs-lookup"><span data-stu-id="76dcd-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="76dcd-128">En este ejemplo se muestran ambas variedades de creación de objetos: la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) genérica y un método ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) que es específico del objeto de cuadro de diálogo de elementos comunes.</span><span class="sxs-lookup"><span data-stu-id="76dcd-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="76dcd-129">Siguientes</span><span class="sxs-lookup"><span data-stu-id="76dcd-129">Next</span></span>

[<span data-ttu-id="76dcd-130">Administrar la duración de un objeto</span><span class="sxs-lookup"><span data-stu-id="76dcd-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="76dcd-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76dcd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76dcd-132">Abrir el ejemplo de cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="76dcd-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 