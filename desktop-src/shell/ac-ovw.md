---
description: La finalización automática expande las cadenas que se han especificado parcialmente en un control de edición en cadenas completas.
title: Usar Autocompletar
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984371"
---
# <a name="using-autocomplete"></a><span data-ttu-id="38a08-103">Usar Autocompletar</span><span class="sxs-lookup"><span data-stu-id="38a08-103">Using Autocomplete</span></span>

<span data-ttu-id="38a08-104">La finalización automática expande las cadenas que se han especificado parcialmente en un [control de edición](/windows/desktop/Controls/edit-controls) en cadenas completas.</span><span class="sxs-lookup"><span data-stu-id="38a08-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="38a08-105">Por ejemplo, cuando un usuario comienza a escribir una dirección URL en el control de edición de direcciones que está incrustado en la barra de herramientas de Windows Internet Explorer, la finalización automática expande la cadena en una o más opciones de dirección URL completas que son coherentes con la cadena parcial existente.</span><span class="sxs-lookup"><span data-stu-id="38a08-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="38a08-106">Una cadena de dirección URL parcial como "MIC" podría expandirse a " https://www.microsoft.com " o " https://www.microsoft.com/windows ".</span><span class="sxs-lookup"><span data-stu-id="38a08-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="38a08-107">La finalización automática se usa normalmente con controles de edición o con controles que tienen un control de edición incrustado, como el control [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .</span><span class="sxs-lookup"><span data-stu-id="38a08-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="38a08-108">Agregar funcionalidad de autocompletar a la aplicación</span><span class="sxs-lookup"><span data-stu-id="38a08-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="38a08-109">Una aplicación puede Agregar funcionalidad de autocompletar a un control de edición de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="38a08-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="38a08-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) es una función sencilla que puede completar una ruta de acceso o dirección URL del archivo.</span><span class="sxs-lookup"><span data-stu-id="38a08-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="38a08-111">La interfaz [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) se expone mediante el objeto autocompletar (CLSID \_ AutoComplete).</span><span class="sxs-lookup"><span data-stu-id="38a08-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="38a08-112">Permite a las aplicaciones inicializar, habilitar y deshabilitar el objeto.</span><span class="sxs-lookup"><span data-stu-id="38a08-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="38a08-113">**IAutoComplete** permite más control sobre los orígenes de autocompletar, incluida la capacidad de agregar un origen personalizado.</span><span class="sxs-lookup"><span data-stu-id="38a08-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="38a08-114">En el resto de este tema se describe el uso de **IAutoComplete**.</span><span class="sxs-lookup"><span data-stu-id="38a08-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="38a08-115">Vea [Cómo habilitar Autocompletar manualmente](how-to-enable-autocomplete-manually.md) para ver ejemplos de uso específicos.</span><span class="sxs-lookup"><span data-stu-id="38a08-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="38a08-116">Modos de autocompletar</span><span class="sxs-lookup"><span data-stu-id="38a08-116">Autocomplete Modes</span></span>

<span data-ttu-id="38a08-117">Al utilizar [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), la finalización automática puede mostrar la cadena completada en dos modos: autoappend y autosugerir.</span><span class="sxs-lookup"><span data-stu-id="38a08-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="38a08-118">Los modos son independientes; puede habilitar una o ambas.</span><span class="sxs-lookup"><span data-stu-id="38a08-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="38a08-119">Para especificar el modo, llame a [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="38a08-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="38a08-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Agregar datos</span><span class="sxs-lookup"><span data-stu-id="38a08-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="38a08-121">En el modo de anexión automática, la finalización automática anexa el resto de la cadena candidata más probable a los caracteres existentes, y resalta los caracteres anexados.</span><span class="sxs-lookup"><span data-stu-id="38a08-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="38a08-122">Si el usuario sigue introduciendo caracteres, se agregan a la cadena parcial existente.</span><span class="sxs-lookup"><span data-stu-id="38a08-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="38a08-123">Si el usuario agrega un carácter que es idéntico al siguiente carácter resaltado, se desactivará el resaltado de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="38a08-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="38a08-124">Los caracteres restantes seguirán resaltados.</span><span class="sxs-lookup"><span data-stu-id="38a08-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="38a08-125">Si el usuario agrega un carácter que no coincide con el siguiente carácter resaltado, la finalización automática intenta generar una nueva cadena candidata basada en la cadena parcial más grande y anexa el resto de la nueva cadena candidata a la cadena parcial actual.</span><span class="sxs-lookup"><span data-stu-id="38a08-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="38a08-126">Si no se puede encontrar ninguna cadena candidata, solo aparecen los caracteres con tipo y el cuadro de edición se comporta como lo haría sin la finalización automática.</span><span class="sxs-lookup"><span data-stu-id="38a08-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="38a08-127">Este proceso continúa hasta que el usuario acepta una cadena.</span><span class="sxs-lookup"><span data-stu-id="38a08-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="38a08-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>AutoSuggest</span><span class="sxs-lookup"><span data-stu-id="38a08-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="38a08-129">En el modo de sugerencia automática, la función de Autocompletar muestra una lista desplegable con una o más cadenas completas sugeridas, debajo del control de edición.</span><span class="sxs-lookup"><span data-stu-id="38a08-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="38a08-130">El usuario puede seleccionar una de las cadenas sugeridas o seguir escribiendo.</span><span class="sxs-lookup"><span data-stu-id="38a08-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="38a08-131">A medida que se progresen los tipos, la lista desplegable podría modificarse en función de la cadena parcial actual.</span><span class="sxs-lookup"><span data-stu-id="38a08-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="38a08-132">Si establece la \_ marca de búsqueda de ACO en [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), AutoComplete proporciona una opción, en la parte inferior de la lista desplegable, para buscar la cadena parcial actual.</span><span class="sxs-lookup"><span data-stu-id="38a08-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="38a08-133">Esta opción se muestra incluso si no hay ninguna cadena sugerida.</span><span class="sxs-lookup"><span data-stu-id="38a08-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="38a08-134">Si el usuario selecciona la opción de búsqueda, la aplicación debe iniciar un motor de búsqueda para ayudar al usuario.</span><span class="sxs-lookup"><span data-stu-id="38a08-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="38a08-135">Usar orígenes predefinidos de autocompletar</span><span class="sxs-lookup"><span data-stu-id="38a08-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="38a08-136">La finalización automática depende de tener un origen que proporcione cadenas que coincidan con la cadena parcial del usuario.</span><span class="sxs-lookup"><span data-stu-id="38a08-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="38a08-137">Tiene la opción de proporcionar un origen personalizado de autocompletar, pero el sistema proporciona varios de los orígenes más comunes.</span><span class="sxs-lookup"><span data-stu-id="38a08-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="38a08-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory</span><span class="sxs-lookup"><span data-stu-id="38a08-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="38a08-139">Origen de autocompletar que coincide con la lista de direcciones URL en la lista de historial del usuario.</span><span class="sxs-lookup"><span data-stu-id="38a08-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="38a08-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU</span><span class="sxs-lookup"><span data-stu-id="38a08-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="38a08-141">Origen de autocompletar que coincide con la lista de direcciones URL en la lista de usuarios usados recientemente.</span><span class="sxs-lookup"><span data-stu-id="38a08-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="38a08-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF</span><span class="sxs-lookup"><span data-stu-id="38a08-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="38a08-143">Origen de autocompletar que coincide con los elementos del espacio de nombres del shell: los archivos del equipo del usuario, así como los elementos de las carpetas virtuales como el panel de control.</span><span class="sxs-lookup"><span data-stu-id="38a08-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="38a08-144">Hay ocasiones en las que, en lugar de liberar inmediatamente los recursos, es posible que desee conservar los punteros de interfaz en los distintos objetos implicados en Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="38a08-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="38a08-145">En concreto, esto se hace cuando desea ajustar el comportamiento de autocompletar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="38a08-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="38a08-146">La instancia más común de esto se produce cuando se usa el \_ objeto CLSID ACListISF, que se completa de forma autocompleta desde el espacio de nombres del shell y tiene la opción ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) de enumerar también desde el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="38a08-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="38a08-147">Por ejemplo, cuando se navega a una nueva carpeta, Internet Explorer cambia el directorio actual de la barra de direcciones y, por tanto, la configuración debe cambiarse de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="38a08-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="38a08-148">Hay dos maneras de especificar el directorio que el \_ objeto ACLISTISF CLSID debe tratar como el directorio actual:</span><span class="sxs-lookup"><span data-stu-id="38a08-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="38a08-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) especifica el directorio a través de un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span><span class="sxs-lookup"><span data-stu-id="38a08-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="38a08-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) especifica el directorio a través de una cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="38a08-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="38a08-151">En los siguientes Supongamos que **PAL** es un puntero a la interfaz [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) de un \_ objeto ACListISF CLSID:</span><span class="sxs-lookup"><span data-stu-id="38a08-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="38a08-152">Usar [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span><span class="sxs-lookup"><span data-stu-id="38a08-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="38a08-153">Para indicar al \_ objeto ACListISF de CLSID que un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) determinado debe tratarse como el directorio actual, puede usar la interfaz [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) del objeto.</span><span class="sxs-lookup"><span data-stu-id="38a08-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="38a08-154">Dado que un **ITEMIDLIST** puede hacer referencia a una carpeta virtual, este método es más flexible que el uso de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span><span class="sxs-lookup"><span data-stu-id="38a08-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="38a08-155">Tenga en cuenta que en los ejemplos siguientes se usa hace plantilla QueryInterface, que permite una lista de parámetros simplificada.</span><span class="sxs-lookup"><span data-stu-id="38a08-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="38a08-156">Usar [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span><span class="sxs-lookup"><span data-stu-id="38a08-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="38a08-157">Para asignar al \_ objeto CLSID ACListISF una ruta de acceso como directorio actual, puede usar la interfaz [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) del objeto.</span><span class="sxs-lookup"><span data-stu-id="38a08-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
