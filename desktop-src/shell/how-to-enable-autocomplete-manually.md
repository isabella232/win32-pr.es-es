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
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="f04c8-103">Cómo habilitar Autocompletar manualmente</span><span class="sxs-lookup"><span data-stu-id="f04c8-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="f04c8-104">Para obtener un control más detallado sobre el comportamiento de autocompletar, o para agregar un origen personalizado de cadenas de autocompletar, debe administrar el objeto AutoComplete.</span><span class="sxs-lookup"><span data-stu-id="f04c8-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="f04c8-105">Puede habilitar Autocompletar manualmente de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="f04c8-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="f04c8-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f04c8-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="f04c8-107">Creación de un objeto AutoComplete sencillo</span><span class="sxs-lookup"><span data-stu-id="f04c8-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="f04c8-108">En los pasos siguientes se muestra cómo crear e inicializar un objeto AutoComplete sencillo.</span><span class="sxs-lookup"><span data-stu-id="f04c8-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="f04c8-109">Un objeto AutoComplete simple completa las cadenas de un solo origen.</span><span class="sxs-lookup"><span data-stu-id="f04c8-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="f04c8-110">La comprobación de errores se ha omitido intencionadamente en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f04c8-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="f04c8-111">Cree el objeto Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="f04c8-112">Cree el origen de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-112">Create the autocomplete source.</span></span> <span data-ttu-id="f04c8-113">Puede usar un [origen Autocompletar predefinido](ac-ovw.md) o puede escribir su propio origen personalizado.</span><span class="sxs-lookup"><span data-stu-id="f04c8-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="f04c8-114">En el código siguiente se usa uno de los orígenes predefinidos de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="f04c8-115">En el código siguiente se usa un origen personalizado de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="f04c8-116">Puede escribir su propio origen de autocompletar implementando un objeto que exponga la interfaz [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) .</span><span class="sxs-lookup"><span data-stu-id="f04c8-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="f04c8-117">Opcionalmente, el objeto también puede implementar las interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) y [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="f04c8-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="f04c8-118">Establezca las opciones en el origen de autocompletar (opcional).</span><span class="sxs-lookup"><span data-stu-id="f04c8-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="f04c8-119">Puede personalizar el comportamiento del origen de autocompletar estableciendo sus opciones si el origen expone la interfaz [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="f04c8-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="f04c8-120">Al usar los orígenes de autocompleta predefinidos, solo ACListISF de CLSID \_ exporta **IACList2**.</span><span class="sxs-lookup"><span data-stu-id="f04c8-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="f04c8-121">Para obtener una lista completa de las opciones y sus valores, vea [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="f04c8-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="f04c8-122">Inicialice el objeto AutoComplete.</span><span class="sxs-lookup"><span data-stu-id="f04c8-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="f04c8-123">En este ejemplo, **hwndEdit** es el identificador de la ventana de control de edición para la que se va a habilitar Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="f04c8-124">Vea [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) para obtener una descripción de los dos parámetros finales no usados.</span><span class="sxs-lookup"><span data-stu-id="f04c8-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="f04c8-125">Establezca las opciones del objeto autocompletar (opcional).</span><span class="sxs-lookup"><span data-stu-id="f04c8-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="f04c8-126">Puede personalizar el comportamiento del objeto Autocompletar estableciendo sus opciones.</span><span class="sxs-lookup"><span data-stu-id="f04c8-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="f04c8-127">Para obtener una lista completa de las opciones y sus valores, consulte la documentación de [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="f04c8-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="f04c8-128">Libera los objetos.</span><span class="sxs-lookup"><span data-stu-id="f04c8-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="f04c8-129">El objeto AutoComplete permanece adjunto al control de edición incluso después de liberarlo.</span><span class="sxs-lookup"><span data-stu-id="f04c8-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="f04c8-130">Si prevé que va a tener acceso a estos objetos más adelante, por ejemplo, si desea cambiar las opciones de autocompletar, no es necesario que las publique en este momento.</span><span class="sxs-lookup"><span data-stu-id="f04c8-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="f04c8-131">Crear un objeto AutoComplete compuesto</span><span class="sxs-lookup"><span data-stu-id="f04c8-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="f04c8-132">Un objeto AutoComplete compuesto coincide con las cadenas de varios orígenes.</span><span class="sxs-lookup"><span data-stu-id="f04c8-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="f04c8-133">Por ejemplo, la barra de direcciones de Windows Internet Explorer usa un objeto de autocompletar compuesto, ya que el usuario puede empezar a escribir el nombre de un archivo o una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f04c8-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="f04c8-134">La mayoría de los pasos implicados en la creación de un objeto AutoComplete compuesto son idénticos a los pasos descritos en "crear un objeto de autocompletar simple".</span><span class="sxs-lookup"><span data-stu-id="f04c8-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="f04c8-135">Estos pasos se indican como tales.</span><span class="sxs-lookup"><span data-stu-id="f04c8-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="f04c8-136">Cree el objeto Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-136">Create the autocomplete object.</span></span> <span data-ttu-id="f04c8-137">Esto es lo mismo que el paso 1 anterior.</span><span class="sxs-lookup"><span data-stu-id="f04c8-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="f04c8-138">Cree el administrador de objetos de origen compuesto Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="f04c8-139">El objeto de origen compuesto Autocompletar permite combinar varios orígenes de autocompletar en un solo origen de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="f04c8-140">Crear y establecer opciones para cada uno de los orígenes de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="f04c8-141">Repita los pasos 2 y 3 anteriores para cada origen.</span><span class="sxs-lookup"><span data-stu-id="f04c8-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="f04c8-142">Adjunte cada origen de autocompletar al administrador de objetos de origen.</span><span class="sxs-lookup"><span data-stu-id="f04c8-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="f04c8-143">Inicialice el objeto AutoComplete.</span><span class="sxs-lookup"><span data-stu-id="f04c8-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="f04c8-144">Esto es lo mismo que el paso 4 anterior, salvo que en lugar de pasar el origen de autocompletar simple a [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), se pasa el administrador de objetos de origen compuesto.</span><span class="sxs-lookup"><span data-stu-id="f04c8-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="f04c8-145">Establezca las opciones del objeto Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="f04c8-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="f04c8-146">Esto es lo mismo que el paso 5 anterior.</span><span class="sxs-lookup"><span data-stu-id="f04c8-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="f04c8-147">Libera los objetos.</span><span class="sxs-lookup"><span data-stu-id="f04c8-147">Release the objects.</span></span>

    <span data-ttu-id="f04c8-148">Como en el caso simple, puede liberar los objetos en cuanto termine de usarlos, pero también puede conservarlos para cambiar opciones más adelante.</span><span class="sxs-lookup"><span data-stu-id="f04c8-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
