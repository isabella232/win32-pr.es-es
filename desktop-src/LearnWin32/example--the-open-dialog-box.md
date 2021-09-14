---
title: Ejemplo del cuadro de diálogo Abrir
description: El ejemplo de formas que hemos estado usando se deriva ligeramente. Vamos a pasar a un objeto COM que puede usar en un programa Windows el cuadro de diálogo Abrir.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159981"
---
# <a name="example-the-open-dialog-box"></a>Ejemplo: Cuadro de diálogo Abrir

El `Shapes` ejemplo que hemos estado usando es bastante contrived. Vamos a pasar a un objeto COM que puede usar en un programa Windows real: el **cuadro de** diálogo Abrir.

![captura de pantalla que muestra el cuadro de diálogo abierto](images/fileopen01.png)

Para mostrar el **cuadro de** diálogo Abrir, un programa puede usar un objeto COM denominado objeto Cuadro de diálogo de elemento común. El cuadro de diálogo Elemento común implementa una interfaz denominada [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), que se declara en el archivo de encabezado Shobjidl.h.

Este es un programa que muestra el **cuadro de** diálogo Abrir al usuario. Si el usuario selecciona un archivo, el programa muestra un cuadro de diálogo que contiene el nombre de archivo.


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



Este código usa algunos conceptos que se describirán más adelante en el módulo, por lo que no se preocupe si no entiende todo aquí. Este es un esquema básico del código:

1.  Llame [**a CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca COM.
2.  Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto Common Item Dialog y obtener un puntero a la interfaz [**IFileOpenDialog del**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) objeto.
3.  Llame al método **Show** del objeto, que muestra el cuadro de diálogo al usuario. Este método se bloquea hasta que el usuario descarta el cuadro de diálogo.
4.  Llame al método [**GetResult del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) objeto. Este método devuelve un puntero a un segundo objeto COM, denominado objeto *de elemento de* Shell. El elemento shell, que implementa la [**interfaz IShellItem,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) representa el archivo seleccionado por el usuario.
5.  Llame al método [**GetDisplayName del elemento**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) de Shell. Este método obtiene la ruta de acceso del archivo, en forma de cadena.
6.  Mostrar un cuadro de mensaje que muestra la ruta de acceso del archivo.
7.  Llame [**a CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) para cancelar la inicialización de la biblioteca COM.

Los pasos 1, 2 y 7 llaman a funciones definidas por la biblioteca COM. Se trata de funciones COM genéricas. Los pasos del 3 al 5 llaman a métodos definidos por el objeto Common Item Dialog.

En este ejemplo se muestran ambas variedades de creación de objetos: la función [**coCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) genérica y un método ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) que es específico del objeto Common Item Dialog.

## <a name="next"></a>Siguientes

[Administrar la duración de un objeto](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Abrir ejemplo de cuadro de diálogo](open-dialog-box-sample.md)
</dt> </dl>

 

 