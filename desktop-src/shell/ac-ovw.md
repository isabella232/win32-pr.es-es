---
description: Autocompletar expande las cadenas que se han especificado parcialmente en un control de edición en cadenas completas.
title: Uso de autocompletar
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468306"
---
# <a name="using-autocomplete"></a>Uso de autocompletar

Autocompletar expande las cadenas que se han especificado parcialmente en un [control de edición](/windows/desktop/Controls/edit-controls) en cadenas completas. Por ejemplo, cuando un usuario empieza a escribir una dirección URL en el control Edición de direcciones que está insertado en la barra de herramientas de Windows Internet Explorer, la función de autocompletar expande la cadena en una o varias opciones de dirección URL completas que son coherentes con la cadena parcial existente. Una cadena de dirección URL parcial como "mic" podría expandirse a " https://www.microsoft.com " o " https://www.microsoft.com/windows ". La función autocompletar se usa normalmente con controles de edición o con controles que tienen un control de edición incrustado, como el control [ComboBoxEx.](/windows/desktop/Controls/comboboxex-control-reference)

## <a name="adding-autocomplete-functionality-to-your-application"></a>Agregar funcionalidad de autocompletar a la aplicación

Una aplicación puede agregar funcionalidad de autocompletar a un control de edición de dos maneras:

-   [**SHAutoComplete es**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) una función sencilla que puede autocompletar una ruta de acceso o una dirección URL de archivo.
-   [**El objeto autocompletar**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) (CLSID AutoComplete) expone la interfaz \_ IAutoComplete. Permite que las aplicaciones inicialicen, habiliten y deshabiliten el objeto. **IAutoComplete** permite un mayor control sobre los orígenes de autocompletar, incluida la capacidad de agregar un origen personalizado. En el resto de este tema se describe el uso de **IAutoComplete.** Consulte [Cómo habilitar autocompletar manualmente para obtener](how-to-enable-autocomplete-manually.md) ejemplos de uso específicos.

## <a name="autocomplete-modes"></a>Modos de autocompletar

Al usar [**IAutoComplete,**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)autocompletar puede mostrar la cadena completada en dos modos: autoappend y autosuggest. Los modos son independientes; puede habilitar o ambos. Para especificar el modo, llame [**a IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Aplicación automática
</dt> <dd>

En el modo de aplicación automática, la función autocompletar anexa el resto de la cadena candidata más probable a los caracteres existentes, resaltando los caracteres anexados. Si el usuario sigue especificando caracteres, se agrega a la cadena parcial existente. Si el usuario agrega un carácter idéntico al siguiente carácter resaltado, se desactivará el resaltado de ese carácter. Los caracteres restantes seguirán resaltados. Si el usuario agrega un carácter que no coincide con el siguiente carácter resaltado, la función de autocompletar intenta generar una nueva cadena candidata basada en la cadena parcial mayor y anexa el resto de la nueva cadena candidata a la cadena parcial actual. Si no se encuentra ninguna cadena candidata, solo aparecen los caracteres con tipo y el cuadro de edición se comporta como lo haría sin autocompletar. Este proceso continúa hasta que el usuario acepta una cadena.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest
</dt> <dd>

En el modo de sugerencia automática, autocompletar muestra una lista desplegable, con una o varias cadenas completas sugeridas, debajo del control de edición. El usuario puede seleccionar una de las cadenas sugeridas o seguir escribiendo. A medida que avanza la escritura, la lista desplegable se puede modificar en función de la cadena parcial actual. Si establece la marca ACO SEARCH en \_ [**IAutoComplete2::SetOptions,**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)autocompletar proporciona una opción, en la parte inferior de la lista desplegable, para buscar la cadena parcial actual. Esta opción se muestra incluso si no hay ninguna cadena sugerida. Si el usuario selecciona la opción de búsqueda, la aplicación debe iniciar un motor de búsqueda para ayudar al usuario.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Usar orígenes predefinidos de autocompletar

La función de autocompletar depende de tener un origen que le proporciona cadenas para que coincidan con la cadena parcial del usuario. Tiene la opción de proporcionar un origen de autocompletar personalizado, pero el sistema proporciona varios de los orígenes más comunes.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory
</dt> <dd>

Origen de autocompletar que coincide con la lista de direcciones URL de la lista Historial del usuario.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU
</dt> <dd>

Origen de autocompletar que coincide con la lista de direcciones URL de la lista Usados recientemente del usuario.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF
</dt> <dd>

Origen de autocompletar que coincide con elementos del espacio de nombres shell: archivos en el equipo del usuario, así como elementos de carpetas virtuales como Panel de control.

</dd> </dl>

Hay ocasiones en las que, en lugar de liberar inmediatamente los recursos, es posible que quiera conservar los punteros de interfaz a los distintos objetos implicados en la función de autocompletar. En concreto, esto se hace cuando se desea ajustar el comportamiento de autocompletar dinámicamente. La instancia más común de esto se produce cuando se usa el objeto ACListISF de CLSID, que se autocompleta desde el espacio de nombres shell y tiene la opción \_ [**(ACLO \_ CURRENTDIR)**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)de enumerar también desde el directorio actual. Por ejemplo, al navegar a una nueva carpeta, Internet Explorer cambia el directorio actual de la barra de direcciones y, por tanto, la configuración debe cambiarse dinámicamente. Hay dos maneras de especificar el directorio que el objeto \_ CLSID ACListISF debe tratar como directorio actual:

-   [**IPersistFolder especifica**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) el directorio a través de [**ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)
-   [**ICurrentWorkingDirectory especifica**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) el directorio a través de una cadena de ruta de acceso.

En el siguiente ejemplo, suponga que **pal** es un puntero a la [**interfaz IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) de un objeto \_ ACListISF de CLSID:

-   Uso [**de IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):

    Para decir al objeto CLSID ACListISF que un ITEMIDLIST determinado debe tratarse como el directorio actual, puede usar la interfaz \_ [**IPersistFolder del**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) objeto. [](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Puesto que **ITEMIDLIST puede** hacer referencia a una carpeta virtual, este método es más flexible que [**usar ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Tenga en cuenta que en los ejemplos siguientes se usa queryInterface con estructura templatada, que permite una lista simplificada de parámetros.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Uso [**de ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):

    Para proporcionar al objeto CLSID ACListISF una ruta de acceso como directorio actual, puede usar la interfaz \_ [**ICurrentWorkingDirectory del**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) objeto.

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

    

 

 
