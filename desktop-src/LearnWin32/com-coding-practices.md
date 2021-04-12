---
title: Prácticas de codificación COM
description: En este tema se describen las formas de hacer que el código COM sea más eficaz y robusto.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149692"
---
# <a name="com-coding-practices"></a>Prácticas de codificación COM

En este tema se describen las formas de hacer que el código COM sea más eficaz y robusto.

-   [El \_ \_ operador uuidof](/windows)
-   [La macro del IID \_ PPV \_ args](/windows)
-   [El patrón SafeRelease](#the-saferelease-pattern)
-   [Punteros inteligentes COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>El \_ \_ operador uuidof

Al compilar el programa, es posible que obtenga errores del vinculador similares a los siguientes:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Este error significa que una constante GUID se declaró con vinculación externa (**extern**) y el vinculador no encontró la definición de la constante. Normalmente, el valor de una constante GUID se exporta desde un archivo de biblioteca estática. Si usa Microsoft Visual C++, puede evitar la necesidad de vincular una biblioteca estática mediante el operador **\_ \_ uuidof** . Este operador es una extensión de lenguaje de Microsoft. Devuelve un valor GUID de una expresión. La expresión puede ser un nombre de tipo de interfaz, un nombre de clase o un puntero de interfaz. Con **\_ \_ uuidof**, puede crear el objeto de cuadro de diálogo de elementos comunes de la siguiente manera:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



El compilador extrae el valor GUID del encabezado, por lo que no se necesita ninguna exportación de la biblioteca.

> [!Note]  
> El valor GUID se asocia al nombre de tipo declarando `__declspec(uuid( ... ))` en el encabezado. Para obtener más información, vea la documentación de **\_ \_ declspec** en la documentación de Visual C++.

 

## <a name="the-iid_ppv_args-macro"></a>La macro del IID \_ PPV \_ args

Vimos que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) requieren la coerción del parámetro final a un tipo **void \* \*** . Esto crea la posibilidad de que un tipo no coincida. Observe el fragmento de código siguiente:


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



Este código solicita la interfaz [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , pero pasa un puntero [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . La expresión **reinterpretar \_ conversión** elude el sistema de tipos de C++, por lo que el compilador no detectará este error. En el mejor de los casos, si el objeto no implementa la interfaz solicitada, la llamada simplemente produce un error. En el peor de los casos, la función se ejecuta correctamente y tiene un puntero que no coincide. En otras palabras, el tipo de puntero no coincide con la vtable real en la memoria. Como puede imaginar, no se puede producir nada bueno en ese momento.

> [!Note]  
> Una *vtable* (tabla de métodos virtuales) es una tabla de punteros de función. El vtable es la forma en que COM enlaza una llamada al método a su implementación en tiempo de ejecución. No casualmente, las vtables son la forma en que la mayoría de los compiladores de C++ implementan métodos virtuales.

 

La macro del [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) ayuda a evitar esta clase de error. Para usar esta macro, reemplace el código siguiente:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



por este:


```C++
IID_PPV_ARGS(&pFileOpen)
```



La macro inserta automáticamente el `__uuidof(IFileOpenDialog)` identificador de interfaz, por lo que se garantiza que coincida con el tipo de puntero. Este es el código modificado (y correcto):


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Puede usar la misma macro con [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>El patrón SafeRelease

El recuento de referencias es uno de los elementos de programación que es muy sencillo, pero también es tedioso, lo que facilita la obtención de un error. Entre los errores típicos se incluyen:

-   No se puede liberar un puntero de interfaz cuando se ha terminado de usarlo. Esta clase de error hará que el programa pierda memoria y otros recursos, ya que los objetos no se destruyen.
-   Llamando a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con un puntero no válido. Por ejemplo, este error puede producirse si el objeto no se ha creado nunca. Esta categoría de error probablemente hará que el programa se bloquee.
-   Desreferenciación de un puntero de interfaz después de llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) . Este error puede provocar que el programa se bloquee. Lo que es peor, puede hacer que el programa se bloquee de forma aleatoria más adelante, lo que dificulta el seguimiento del error original.

Una manera de evitar estos errores es llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) a través de una función que libera el puntero de forma segura. En el código siguiente se muestra una función que lo hace:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



Esta función toma un puntero de interfaz COM como parámetro y hace lo siguiente:

1.  Comprueba si el puntero es **null**.
2.  Llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) si el puntero no es **null**.
3.  Establece el puntero en **null**.

A continuación se muestra un ejemplo de cómo usar `SafeRelease` :


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



Si [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) se realiza correctamente, la llamada a `SafeRelease` libera el puntero. Si se produce un error de **CoCreateInstance** , *PFileOpen* sigue siendo **null**. La `SafeRelease` función comprueba esto y omite la llamada a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

También es seguro llamar a `SafeRelease` más de una vez en el mismo puntero, como se muestra aquí:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Punteros inteligentes COM

La `SafeRelease` función es útil, pero requiere que recuerde dos cosas:

-   Inicialice todos los punteros de interfaz en **null**.
-   Llame a `SafeRelease` antes de que cada puntero salga del ámbito.

Como programador de C++, es probable que piense que no debe recordar nada de esto. Después de todo, este es el motivo por el que C++ tiene constructores y destructores. Estaría bien tener una clase que contiene el puntero de interfaz subyacente e inicializa y libera automáticamente el puntero. En otras palabras, queremos algo parecido a esto:


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



La definición de clase que se muestra aquí está incompleta y no se puede usar como se muestra. Como mínimo, debe definir un constructor de copias, un operador de asignación y una manera de tener acceso al puntero COM subyacente. Afortunadamente, no es necesario realizar ninguna tarea, ya que Microsoft Visual Studio ya proporciona una clase de puntero inteligente como parte del Active Template Library (ATL).

La clase de puntero inteligente ATL se denomina **CComPtr**. (También hay una clase **CComQIPtr** , que no se trata aquí). Este es el ejemplo de [cuadro de diálogo Abrir](example--the-open-dialog-box.md) que se ha vuelto a escribir para usar **CComPtr**.


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



La diferencia principal entre este código y el ejemplo original es que esta versión no llama explícitamente a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Cuando la instancia de **CComPtr** sale del ámbito, el destructor llama a **Release** en el puntero subyacente.

**CComPtr** es una plantilla de clase. El argumento de plantilla es el tipo de interfaz COM. Internamente, **CComPtr** contiene un puntero de ese tipo. **CComPtr** invalida **Operator-> ()** y **Operator& ()** para que la clase actúe como el puntero subyacente. Por ejemplo, el código siguiente es equivalente a llamar al método **IFileOpenDialog:: show** directamente:


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** también define un método **CComPtr:: CoCreateInstance** , que llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) de com con algunos valores de parámetro predeterminados. El único parámetro necesario es el identificador de clase, como se muestra en el ejemplo siguiente:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



El método **CComPtr:: CoCreateInstance** se proporciona únicamente por comodidad; puede seguir llamando a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) de com, si lo prefiere.

## <a name="next"></a>Siguientes

[Control de errores en COM](error-handling-in-com.md)

 

 