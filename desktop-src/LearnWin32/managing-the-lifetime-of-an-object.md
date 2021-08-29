---
title: Administrar la duración de un objeto
description: Obtenga información sobre cómo administrar los métodos AddRef y Release para controlar la duración de un objeto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a10ec4e7a873c5e8b86c3d2bfe91fd1531051d599831151d3dbec5ed3d70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897444"
---
# <a name="managing-the-lifetime-of-an-object"></a>Administrar la duración de un objeto

Hay una regla para las interfaces COM que todavía no hemos mencionado. Cada interfaz COM debe heredar, directa o indirectamente, de una interfaz denominada [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Esta interfaz proporciona algunas funcionalidades de línea base que todos los objetos COM deben admitir.

La [**interfaz IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) define tres métodos:

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

El [**método QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permite a un programa consultar las funciones del objeto en tiempo de ejecución. Vamos a decir más sobre esto en el tema siguiente, [Asking an Object for an Interface](asking-an-object-for-an-interface.md). Los [**métodos AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**y Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se usan para controlar la duración de un objeto. Este es el tema de este tema.

## <a name="reference-counting"></a>Recuento de referencias

Cualquier otra cosa que pueda hacer un programa, en algún momento asignará y liberará recursos. Asignar un recurso es fácil. Saber cuándo liberar el recurso es difícil, especialmente si la duración del recurso se extiende más allá del ámbito actual. Este problema no es exclusivo de COM. Cualquier programa que asigne memoria del montón debe resolver el mismo problema. Por ejemplo, C++ usa destructores automáticos, mientras que C# y Java usan la recolección de elementos no utilizados. COM usa un enfoque denominado *recuento de referencias.*

Cada objeto COM mantiene un recuento interno. Esto se conoce como recuento de referencias. El recuento de referencias realiza un seguimiento de cuántas referencias al objeto están activas actualmente. Cuando el número de referencias cae a cero, el objeto se elimina a sí mismo. Merece la pena repetir la última parte: el objeto se elimina a sí mismo. El programa nunca elimina explícitamente el objeto.

Estas son las reglas para el recuento de referencias:

-   Cuando se crea el objeto por primera vez, su recuento de referencias es 1. En este momento, el programa tiene un puntero único al objeto .
-   El programa puede crear una nueva referencia duplicando (copiando) el puntero. Al copiar el puntero, debe llamar al [**método AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) del objeto . Este método incrementa el recuento de referencias en uno.
-   Cuando haya terminado de usar un puntero al objeto , debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). El **método Release** disminuye el recuento de referencias en uno. También invalida el puntero. No vuelva a usar el puntero después de llamar a **Release**. (Si tiene otros punteros al mismo objeto, puede seguir usando esos punteros).
-   Cuando se ha llamado [**a Release con**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cada puntero, el recuento de referencias de objeto del objeto alcanza cero y el objeto se elimina a sí mismo.

En el diagrama siguiente se muestra un caso sencillo pero típico.

![Diagrama que muestra un caso simple de recuento de referencias.](images/com04.png)

El programa crea un objeto y almacena un puntero *(p*) al objeto . En este momento, el recuento de referencias es 1. Cuando el programa termina de usar el puntero , llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). El recuento de referencias se disminuye a cero y el objeto se elimina a sí mismo. Ahora *p* no es válido. Es un error usar *p* para cualquier otra llamada de método.

En el diagrama siguiente se muestra un ejemplo más complejo.

![ilustración que muestra el recuento de referencias](images/com05.png)

En este caso, el programa crea un objeto y almacena el puntero *p*, como antes. A continuación, el programa *copia p* en una nueva variable, *q*. En este momento, el programa debe llamar a [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento de referencias. El recuento de referencias es ahora 2 y hay dos punteros válidos al objeto . Ahora supongamos que el programa ha terminado de usar *p*. El programa llama [**a Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), el recuento de referencias va a 1 y *p* ya no es válido. Sin embargo, *q* sigue siendo válido. Más adelante, el programa termina de usar *q*. Por lo tanto, vuelve a **llamar a Release.** El recuento de referencias va a cero y el objeto se elimina a sí mismo.

Es posible que se pregunte por qué el programa copiaría *p*. Hay dos razones principales: en primer lugar, es posible que desee almacenar el puntero en una estructura de datos, como una lista. En segundo lugar, es posible que desee mantener el puntero más allá del ámbito actual de la variable original. Por lo tanto, se copiaría en una nueva variable con un ámbito más amplio.

Una ventaja del recuento de referencias es que puede compartir punteros en diferentes secciones de código, sin que las distintas rutas de acceso de código se coordine para eliminar el objeto. En su lugar, cada ruta de acceso de código simplemente llama [**a Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando esa ruta de acceso de código se realiza mediante el objeto . El objeto controla la eliminación en el momento correcto.

## <a name="example"></a>Ejemplo

Este es el código del ejemplo de [cuadro de diálogo](example--the-open-dialog-box.md) Abrir de nuevo.

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

El recuento de referencias se produce en dos lugares de este código. En primer lugar, si el programa crea correctamente el objeto Cuadro de diálogo de elemento común, debe llamar a [**Release en**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) el *puntero pFileOpen.*

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

En segundo lugar, cuando [**el método GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) devuelve un puntero a la interfaz [**IShellItem,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) el programa debe llamar a [**Release en**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) el *puntero pItem.*

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Tenga en cuenta que, en ambos casos, la [**llamada release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) es lo último que ocurre antes de que el puntero salga del ámbito. Observe también que **solo se llama** a Release después de probar el **HRESULT** para comprobar que se ha hecho correctamente. Por ejemplo, si se produce un error en la llamada a [**CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) el *puntero pFileOpen* no es válido. Por lo tanto, sería un error llamar a **Release en** el puntero.

## <a name="next"></a>Siguientes

[Pedir un objeto para una interfaz](asking-an-object-for-an-interface.md)