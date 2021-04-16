---
title: Administrar la duración de un objeto
description: Obtenga información sobre cómo administrar los métodos AddRef y RELEASE para controlar la duración de un objeto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557141"
---
# <a name="managing-the-lifetime-of-an-object"></a>Administrar la duración de un objeto

Hay una regla para las interfaces COM que todavía no hemos mencionado. Cada interfaz COM debe heredar, directa o indirectamente, de una interfaz denominada [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Esta interfaz proporciona algunas funciones de línea base que todos los objetos COM deben admitir.

La interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) define tres métodos:

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

El método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permite a un programa consultar las capacidades del objeto en tiempo de ejecución. En el tema siguiente se indicará más sobre eso, [donde se pide un objeto para una interfaz](asking-an-object-for-an-interface.md). Los métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se utilizan para controlar la duración de un objeto. Este es el asunto de este tema.

## <a name="reference-counting"></a>Recuento de referencias

Lo que pueda hacer un programa, en algún momento se asignarán y liberarán recursos. Es fácil asignar un recurso. Saber cuándo liberar el recurso es difícil, especialmente si la duración del recurso se extiende más allá del ámbito actual. Este problema no es único para COM. Cualquier programa que asigne memoria del montón debe resolver el mismo problema. Por ejemplo, C++ usa destructores automáticos, mientras que C# y Java usan la recolección de elementos no utilizados. COM utiliza un enfoque denominado *recuento de referencias*.

Cada objeto COM mantiene un recuento interno. Esto se conoce como recuento de referencias. El recuento de referencias realiza un seguimiento del número de referencias al objeto que están activas actualmente. Cuando el número de referencias cae a cero, el objeto se elimina a sí mismo. Merece la pena repetir la última parte: el objeto se elimina a sí mismo. El programa no elimina nunca explícitamente el objeto.

Estas son las reglas para el recuento de referencias:

-   Cuando el objeto se crea por primera vez, su recuento de referencias es 1. En este punto, el programa tiene un único puntero al objeto.
-   El programa puede crear una nueva referencia duplicando (copiando) el puntero. Al copiar el puntero, debe llamar al método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) del objeto. Este método incrementa el recuento de referencias en uno.
-   Cuando haya terminado de usar un puntero al objeto, debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). El método **Release** reduce el recuento de referencias en uno. También invalida el puntero. No vuelva a usar el puntero después de llamar a **Release**. (Si tiene otros punteros al mismo objeto, puede seguir usando esos punteros).
-   Cuando se ha llamado a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con cada puntero, el recuento de referencias de objeto del objeto alcanza el valor cero y el objeto se elimina a sí mismo.

En el diagrama siguiente se muestra un caso sencillo pero típico.

![Diagrama que muestra un caso simple de recuento de referencias.](images/com04.png)

El programa crea un objeto y almacena un puntero (*p*) en el objeto. En este punto, el recuento de referencias es 1. Cuando el programa termina de usar el puntero, llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). El recuento de referencias se reduce a cero y el objeto se elimina a sí mismo. Ahora *p* no es válido. Es un error usar *p* para otras llamadas a métodos.

En el diagrama siguiente se muestra un ejemplo más complejo.

![Ilustración que muestra el recuento de referencias](images/com05.png)

En este caso, el programa crea un objeto y almacena el puntero *p*, como antes. Después, el programa copia *p* en una nueva variable, *q*. En este momento, el programa debe llamar a [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento de referencias. Ahora, el recuento de referencias es 2 y hay dos punteros válidos al objeto. Ahora Supongamos que el programa ha terminado de usar *p*. El programa llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), el recuento de referencias va a 1 y *p* ya no es válido. Sin embargo, *q* sigue siendo válido. Más adelante, el programa termina de usar *q*. Por lo tanto, vuelve a llamar a **Release** . El recuento de referencias llega a cero y el objeto se elimina a sí mismo.

Es posible que se pregunte por qué el programa copiará *p*. Hay dos razones principales: en primer lugar, puede que desee almacenar el puntero en una estructura de datos, como una lista. En segundo lugar, puede que desee mantener el puntero más allá del ámbito actual de la variable original. Por lo tanto, se copiará en una nueva variable con un ámbito más amplio.

Una ventaja del recuento de referencias es que puede compartir punteros en diferentes secciones de código, sin las distintas rutas de acceso de código que se coordinan para eliminar el objeto. En su lugar, cada ruta de acceso de código simplemente llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando la ruta de acceso del código se realiza mediante el objeto. El objeto controla la eliminación en el momento correcto.

## <a name="example"></a>Ejemplo

Este es el código del [ejemplo de cuadro de diálogo Abrir](example--the-open-dialog-box.md) de nuevo.

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

El recuento de referencias se produce en dos lugares en este código. En primer lugar, si el programa crea correctamente el objeto de cuadro de diálogo de elementos comunes, debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pFileOpen* .

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

En segundo lugar, cuando el método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) devuelve un puntero a la interfaz [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , el programa debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pItem* .

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Observe que, en ambos casos, la llamada de [**versión**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) es lo último que ocurre antes de que el puntero salga del ámbito. Observe también que solo se llama a **Release** después de probar el **valor de HRESULT** para ver si se ha realizado correctamente. Por ejemplo, si se produce un error en la llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , el puntero *pFileOpen* no es válido. Por lo tanto, sería un error llamar a **Release** en el puntero.

## <a name="next"></a>Siguientes

[Solicitar un objeto para una interfaz](asking-an-object-for-an-interface.md)