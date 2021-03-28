---
description: Para obtener un control más detallado sobre el comportamiento de autocompletar, o para agregar un origen personalizado de cadenas de autocompletar, debe administrar el objeto AutoComplete.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Cómo habilitar Autocompletar manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985446"
---
# <a name="how-to-enable-autocomplete-manually"></a>Cómo habilitar Autocompletar manualmente

Para obtener un control más detallado sobre el comportamiento de autocompletar, o para agregar un origen personalizado de cadenas de autocompletar, debe administrar el objeto AutoComplete. Puede habilitar Autocompletar manualmente de las siguientes maneras.

## <a name="instructions"></a>Instrucciones

### <a name="creating-a-simple-autocomplete-object"></a>Creación de un objeto AutoComplete sencillo

En los pasos siguientes se muestra cómo crear e inicializar un objeto AutoComplete sencillo. Un objeto AutoComplete simple completa las cadenas de un solo origen. La comprobación de errores se ha omitido intencionadamente en este ejemplo.

1.  Cree el objeto Autocompletar.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Cree el origen de autocompletar. Puede usar un [origen Autocompletar predefinido](ac-ovw.md) o puede escribir su propio origen personalizado.

    En el código siguiente se usa uno de los orígenes predefinidos de autocompletar.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    En el código siguiente se usa un origen personalizado de autocompletar. Puede escribir su propio origen de autocompletar implementando un objeto que exponga la interfaz [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) . Opcionalmente, el objeto también puede implementar las interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) y [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .

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

    Puede personalizar el comportamiento del origen de autocompletar estableciendo sus opciones si el origen expone la interfaz [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) . Al usar los orígenes de autocompleta predefinidos, solo ACListISF de CLSID \_ exporta **IACList2**. Para obtener una lista completa de las opciones y sus valores, vea [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Inicialice el objeto AutoComplete.

    En este ejemplo, **hwndEdit** es el identificador de la ventana de control de edición para la que se va a habilitar Autocompletar. Vea [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) para obtener una descripción de los dos parámetros finales no usados.

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Establezca las opciones del objeto autocompletar (opcional).

    Puede personalizar el comportamiento del objeto Autocompletar estableciendo sus opciones. Para obtener una lista completa de las opciones y sus valores, consulte la documentación de [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Libera los objetos.

    > [!Note]  
    > El objeto AutoComplete permanece adjunto al control de edición incluso después de liberarlo. Si prevé que va a tener acceso a estos objetos más adelante, por ejemplo, si desea cambiar las opciones de autocompletar, no es necesario que las publique en este momento.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Crear un objeto AutoComplete compuesto

Un objeto AutoComplete compuesto coincide con las cadenas de varios orígenes. Por ejemplo, la barra de direcciones de Windows Internet Explorer usa un objeto de autocompletar compuesto, ya que el usuario puede empezar a escribir el nombre de un archivo o una dirección URL. La mayoría de los pasos implicados en la creación de un objeto AutoComplete compuesto son idénticos a los pasos descritos en "crear un objeto de autocompletar simple". Estos pasos se indican como tales.

1.  Cree el objeto Autocompletar. Esto es lo mismo que el paso 1 anterior.

2.  Cree el administrador de objetos de origen compuesto Autocompletar.

    El objeto de origen compuesto Autocompletar permite combinar varios orígenes de autocompletar en un solo origen de autocompletar.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Crear y establecer opciones para cada uno de los orígenes de autocompletar. Repita los pasos 2 y 3 anteriores para cada origen.

4.  Adjunte cada origen de autocompletar al administrador de objetos de origen.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Inicialice el objeto AutoComplete.

    Esto es lo mismo que el paso 4 anterior, salvo que en lugar de pasar el origen de autocompletar simple a [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), se pasa el administrador de objetos de origen compuesto.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Establezca las opciones del objeto Autocompletar. Esto es lo mismo que el paso 5 anterior.

7.  Libera los objetos.

    Como en el caso simple, puede liberar los objetos en cuanto termine de usarlos, pero también puede conservarlos para cambiar opciones más adelante.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
