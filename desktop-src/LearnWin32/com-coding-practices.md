---
title: Prácticas de codificación COM
description: En este tema se describen formas de hacer que el código COM sea más eficaz y sólido.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93febc4ee3dfd4f05f20fae8078bc2a5ebb7f9623a860f49ec9cd6ce4e69b95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913895"
---
# <a name="com-coding-practices"></a>Prácticas de codificación COM

En este tema se describen formas de hacer que el código COM sea más eficaz y sólido.

-   [Operador \_ \_ uuidof](/windows)
-   [Macro \_ ARGS de IID PPV \_](/windows)
-   [El patrón SafeRelease](#the-saferelease-pattern)
-   [Punteros inteligentes COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>Operador \_ \_ uuidof

Al compilar el programa, es posible que obtenga errores del vinculador similares a los siguientes:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Este error significa que se declaró una constante GUID con vinculación externa **(extern**) y el vinculador no pudo encontrar la definición de la constante. El valor de una constante GUID normalmente se exporta desde un archivo de biblioteca estática. Si usa Microsoft Visual C++, puede evitar la necesidad de vincular una biblioteca estática mediante el **\_ \_ operador uuidof.** Este operador es una extensión de lenguaje de Microsoft. Devuelve un valor GUID de una expresión. La expresión puede ser un nombre de tipo de interfaz, un nombre de clase o un puntero de interfaz. Con **\_ \_ uuidof**, puede crear el objeto De diálogo de elemento común de la siguiente manera:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



El compilador extrae el valor GUID del encabezado, por lo que no es necesaria ninguna exportación de biblioteca.

> [!Note]  
> El valor GUID está asociado al nombre de tipo declarando `__declspec(uuid( ... ))` en el encabezado . Para obtener más información, consulte la documentación de **\_ \_ declspec** en la documentación Visual C++ datos.

 

## <a name="the-iid_ppv_args-macro"></a>Macro \_ ARGS de IID PPV \_

Vimos que [**Tanto CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) como [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) requieren la coerción del parámetro final a un **tipo \* \* void.** Esto crea la posibilidad de un error de coincidencia de tipos. Observe el fragmento de código siguiente:


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



Este código solicita la [**interfaz IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pero pasa un [**puntero IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) La **expresión de \_ conversión reinterpretación** evita el sistema de tipos de C++, por lo que el compilador no detectará este error. En el mejor de los casos, si el objeto no implementa la interfaz solicitada, la llamada simplemente produce un error. En el peor de los casos, la función se realiza correctamente y tiene un puntero no coincidente. En otras palabras, el tipo de puntero no coincide con la vtable real en memoria. Como puede imaginar, no puede pasar nada bueno en ese momento.

> [!Note]  
> Una *tabla vtable* (tabla de métodos virtuales) es una tabla de punteros de función. La tabla virtual es cómo COM enlaza una llamada de método a su implementación en tiempo de ejecución. Por coincidencia, las tablas virtuales son la forma en que la mayoría de los compiladores de C++ implementan métodos virtuales.

 

La [**macro \_ \_ ARGS de IID PPV**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) ayuda a evitar esta clase de error. Para usar esta macro, reemplace el código siguiente:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



por este:


```C++
IID_PPV_ARGS(&pFileOpen)
```



La macro se inserta automáticamente para el identificador de interfaz, por lo que se garantiza `__uuidof(IFileOpenDialog)` que coincide con el tipo de puntero. Este es el código modificado (y correcto):


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

El recuento de referencias es una de esas cosas de la programación que es básicamente fácil, pero también tediosa, lo que facilita el error. Entre los errores típicos se incluyen:

-   No se puede liberar un puntero de interfaz cuando haya terminado de usarlo. Esta clase de error hará que el programa filtre memoria y otros recursos, ya que los objetos no se destruyen.
-   Llamar [**a Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con un puntero no válido. Por ejemplo, este error puede producirse si el objeto nunca se creó. Esta categoría de error probablemente hará que el programa se bloquea.
-   Desreferenciar un puntero de interfaz después [**de llamar a**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) Release. Este error puede hacer que el programa se bloquea. Lo que es peor, puede hacer que el programa se bloquee de forma aleatoria más adelante, lo que hace que sea difícil realizar un seguimiento del error original.

Una manera de evitar estos errores es llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) a través de una función que libera el puntero de forma segura. El código siguiente muestra una función que hace esto:


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

1.  Comprueba si el puntero es **NULL.**
2.  Llama [**a Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) si el puntero no es **NULL.**
3.  Establece el puntero en **NULL.**

Este es un ejemplo de cómo usar `SafeRelease` :


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



Si [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) se realiza correctamente, la llamada `SafeRelease` a libera el puntero. Si se produce un error **en CoCreateInstance,** *pFileOpen* sigue **siendo NULL.** La `SafeRelease` función lo comprueba y omite la llamada a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

También es seguro llamar a `SafeRelease` más de una vez en el mismo puntero, como se muestra aquí:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Punteros inteligentes COM

La `SafeRelease` función es útil, pero requiere que recuerde dos cosas:

-   Inicialice cada puntero de interfaz en **NULL.**
-   Llame `SafeRelease` a antes de que cada puntero salga del ámbito.

Como programador de C++, probablemente piense que no debería tener que recordar ninguna de estas cosas. Después de todo, por eso C++ tiene constructores y destructores. Sería bueno tener una clase que encapsula el puntero de interfaz subyacente e inicializa y libera automáticamente el puntero. En otras palabras, queremos algo parecido a esto:


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



La definición de clase que se muestra aquí está incompleta y no es utilizable como se muestra. Como mínimo, tendría que definir un constructor de copia, un operador de asignación y una manera de acceder al puntero COM subyacente. Afortunadamente, no es necesario realizar nada de este trabajo, ya que Microsoft Visual Studio proporciona una clase de puntero inteligente como parte del Active Template Library (ATL).

La clase de puntero inteligente ATL se denomina **CComPtr**. (También hay una **clase CComQIPtr,** que no se describe aquí). Este es el ejemplo [abrir cuadro de diálogo](example--the-open-dialog-box.md) reescrito para usar **CComPtr**.


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



La principal diferencia entre este código y el ejemplo original es que esta versión no llama explícitamente a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Cuando la **instancia de CComPtr** sale del ámbito, el destructor llama **a Release en** el puntero subyacente.

**CComPtr es** una plantilla de clase. El argumento de plantilla es el tipo de interfaz COM. Internamente, **CComPtr** contiene un puntero de ese tipo. **CComPtr** invalida **operator->()** y **operator&()** para que la clase actúe como el puntero subyacente. Por ejemplo, el código siguiente equivale a llamar al método **IFileOpenDialog::Show** directamente:


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr también** define un **método CComPtr::CoCreateInstance,** que llama a la función [**COM CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con algunos valores de parámetro predeterminados. El único parámetro necesario es el identificador de clase, como se muestra en el ejemplo siguiente:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



El **método CComPtr::CoCreateInstance** se proporciona únicamente por comodidad; Todavía puede llamar a la función [**COCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) de COM, si lo prefiere.

## <a name="next"></a>Siguientes

[Control de errores en COM](error-handling-in-com.md)

 

 