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
# <a name="example-the-open-dialog-box"></a>Ejemplo: el cuadro de diálogo abrir

El `Shapes` ejemplo que se ha usado es algo inventado. Vamos a convertir un objeto COM que puede usar en un programa real de Windows: el cuadro de diálogo **abrir** .

![captura de pantalla que muestra el cuadro de diálogo abrir](images/fileopen01.png)

Para mostrar el cuadro de diálogo **abrir** , un programa puede utilizar un objeto com denominado el objeto de cuadro de diálogo de elementos comunes. El cuadro de diálogo Common Item implementa una interfaz denominada [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), que se declara en el archivo de encabezado shobjidl. h.

Este es un programa que muestra el cuadro de diálogo **abrir** al usuario. Si el usuario selecciona un archivo, el programa muestra un cuadro de diálogo que contiene el nombre de archivo.


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



Este código usa algunos conceptos que se describirán más adelante en el módulo, por lo que no se preocupe si no comprende todo aquí. Este es un esquema básico del código:

1.  Llame a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com.
2.  Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto de cuadro de diálogo de elementos comunes y obtener un puntero a la interfaz [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) del objeto.
3.  Llame al método **Show** del objeto, que muestra el cuadro de diálogo al usuario. Este método se bloquea hasta que el usuario descarta el cuadro de diálogo.
4.  Llame al método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) del objeto. Este método devuelve un puntero a un segundo objeto COM, denominado objeto de *elemento de Shell* . El elemento de Shell, que implementa la interfaz [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , representa el archivo seleccionado por el usuario.
5.  Llame al método [**getDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) del elemento de Shell. Este método obtiene la ruta de acceso del archivo, en forma de cadena.
6.  Muestra un cuadro de mensaje que muestra la ruta de acceso del archivo.
7.  Llame a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) para anular la inicialización de la biblioteca com.

Los pasos 1, 2 y 7 llaman a las funciones definidas por la biblioteca COM. Se trata de funciones COM genéricas. Los pasos 3 a 5 llaman a los métodos definidos por el objeto de cuadro de diálogo de elementos comunes.

En este ejemplo se muestran ambas variedades de creación de objetos: la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) genérica y un método ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) que es específico del objeto de cuadro de diálogo de elementos comunes.

## <a name="next"></a>Siguientes

[Administrar la duración de un objeto](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Abrir el ejemplo de cuadro de diálogo](open-dialog-box-sample.md)
</dt> </dl>

 

 