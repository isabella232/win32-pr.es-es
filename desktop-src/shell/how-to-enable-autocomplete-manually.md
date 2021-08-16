---
description: Para obtener un control más detallado sobre el comportamiento de autocompletar o para agregar un origen personalizado de cadenas de autocompletar, debe administrar el objeto autocompletar usted mismo.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Cómo habilitar autocompletar manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7df686e4c5a4a6e96b1faf82e4926dffc73398b360e3e6235d6a61451eae189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859712"
---
# <a name="how-to-enable-autocomplete-manually"></a>Cómo habilitar autocompletar manualmente

Para obtener un control más detallado sobre el comportamiento de autocompletar o para agregar un origen personalizado de cadenas de autocompletar, debe administrar el objeto autocompletar usted mismo. Puede habilitar autocompletar manualmente de las maneras siguientes.

## <a name="instructions"></a>Instructions

### <a name="creating-a-simple-autocomplete-object"></a>Crear un objeto autocompletar simple

En los pasos siguientes se muestra cómo crear e inicializar un objeto autocompletar simple. Un objeto autocompletar simple completa las cadenas de un único origen. La comprobación de errores se ha omitido intencionadamente en este ejemplo.

1.  Cree el objeto autocompletar.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Cree el origen de autocompletar. Puede usar un [origen predefinido de autocompletar](ac-ovw.md) o escribir su propio origen personalizado.

    El código siguiente usa uno de los orígenes predefinidos de autocompletar.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    El código siguiente usa un origen de autocompletar personalizado. Puede escribir su propio origen de autocompletar implementando un objeto que expone la [**interfaz IEnumString.**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) El objeto también puede implementar opcionalmente las interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) [**e IACList2.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Establezca las opciones en el origen de autocompletar (opcional).

    Puede personalizar el comportamiento del origen de autocompletar estableciendo sus opciones si el origen expone la [**interfaz IACList2.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) Cuando se usan los orígenes predefinidos de autocompletar, solo CLSID \_ ACListISF exporta **IACList2**. Para obtener una lista completa de las opciones y sus valores, vea [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Inicialice el objeto autocompletar.

    En este ejemplo, **hwndEdit es** el identificador de la ventana de control de edición para la que se va a habilitar la función de autocompletar. Vea [**IAutoComplete::Init para**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) obtener una descripción de los dos últimos parámetros no usados.

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Establezca las opciones del objeto autocompletar (opcional).

    Puede personalizar el comportamiento del objeto autocompletar estableciendo sus opciones. Para obtener una lista completa de las opciones y sus valores, vea la documentación de [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Libere los objetos .

    > [!Note]  
    > El objeto autocompletar permanece asociado al control de edición incluso después de liberarlo. Si prevé la necesidad de acceder a estos objetos más adelante,si desea cambiar las opciones de autocompletar más adelante, por ejemplo, no es necesario liberarlos en este momento.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Crear un objeto autocompletar compuesto

Un objeto de autocompletar compuesto coincide con cadenas de varios orígenes. Por ejemplo, la Windows Internet Explorer address usa un objeto de autocompletar compuesto porque el usuario podría empezar a escribir el nombre de un archivo o una dirección URL. La mayoría de los pasos implicados en la creación de un objeto de autocompletar compuesto son idénticos a los pasos de "Crear un objeto de autocompletar simple". Estos pasos se indican como tales.

1.  Cree el objeto autocompletar. Esto es lo mismo que en el paso 1 anterior.

2.  Cree el administrador de objetos de origen compuesto autocompletar.

    El objeto de origen compuesto autocompletar permite combinar varios orígenes de autocompletar en un único origen de autocompletar.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Cree y establezca opciones para cada uno de los orígenes de autocompletar. Repita los pasos 2 y 3 anteriores para cada origen.

4.  Adjunte cada origen de autocompletar al administrador de objetos de origen.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Inicialice el objeto autocompletar.

    Esto es lo mismo que en el paso 4 anterior, salvo que, en lugar de pasar el origen de autocompletar simple a [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), se pasa el administrador de objetos de origen compuesto.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Establezca las opciones del objeto autocompletar. Esto es lo mismo que en el paso 5 anterior.

7.  Libere los objetos .

    Como en el caso simple, puede liberar los objetos en cuanto haya terminado de usarlos, pero también puede conservarlos para cambiar las opciones más adelante.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
