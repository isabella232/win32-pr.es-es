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
# <a name="using-autocomplete"></a>Usar Autocompletar

La finalización automática expande las cadenas que se han especificado parcialmente en un [control de edición](/windows/desktop/Controls/edit-controls) en cadenas completas. Por ejemplo, cuando un usuario comienza a escribir una dirección URL en el control de edición de direcciones que está incrustado en la barra de herramientas de Windows Internet Explorer, la finalización automática expande la cadena en una o más opciones de dirección URL completas que son coherentes con la cadena parcial existente. Una cadena de dirección URL parcial como "MIC" podría expandirse a " https://www.microsoft.com " o " https://www.microsoft.com/windows ". La finalización automática se usa normalmente con controles de edición o con controles que tienen un control de edición incrustado, como el control [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .

## <a name="adding-autocomplete-functionality-to-your-application"></a>Agregar funcionalidad de autocompletar a la aplicación

Una aplicación puede Agregar funcionalidad de autocompletar a un control de edición de dos maneras:

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) es una función sencilla que puede completar una ruta de acceso o dirección URL del archivo.
-   La interfaz [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) se expone mediante el objeto autocompletar (CLSID \_ AutoComplete). Permite a las aplicaciones inicializar, habilitar y deshabilitar el objeto. **IAutoComplete** permite más control sobre los orígenes de autocompletar, incluida la capacidad de agregar un origen personalizado. En el resto de este tema se describe el uso de **IAutoComplete**. Vea [Cómo habilitar Autocompletar manualmente](how-to-enable-autocomplete-manually.md) para ver ejemplos de uso específicos.

## <a name="autocomplete-modes"></a>Modos de autocompletar

Al utilizar [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), la finalización automática puede mostrar la cadena completada en dos modos: autoappend y autosugerir. Los modos son independientes; puede habilitar una o ambas. Para especificar el modo, llame a [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Agregar datos
</dt> <dd>

En el modo de anexión automática, la finalización automática anexa el resto de la cadena candidata más probable a los caracteres existentes, y resalta los caracteres anexados. Si el usuario sigue introduciendo caracteres, se agregan a la cadena parcial existente. Si el usuario agrega un carácter que es idéntico al siguiente carácter resaltado, se desactivará el resaltado de ese carácter. Los caracteres restantes seguirán resaltados. Si el usuario agrega un carácter que no coincide con el siguiente carácter resaltado, la finalización automática intenta generar una nueva cadena candidata basada en la cadena parcial más grande y anexa el resto de la nueva cadena candidata a la cadena parcial actual. Si no se puede encontrar ninguna cadena candidata, solo aparecen los caracteres con tipo y el cuadro de edición se comporta como lo haría sin la finalización automática. Este proceso continúa hasta que el usuario acepta una cadena.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>AutoSuggest
</dt> <dd>

En el modo de sugerencia automática, la función de Autocompletar muestra una lista desplegable con una o más cadenas completas sugeridas, debajo del control de edición. El usuario puede seleccionar una de las cadenas sugeridas o seguir escribiendo. A medida que se progresen los tipos, la lista desplegable podría modificarse en función de la cadena parcial actual. Si establece la \_ marca de búsqueda de ACO en [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), AutoComplete proporciona una opción, en la parte inferior de la lista desplegable, para buscar la cadena parcial actual. Esta opción se muestra incluso si no hay ninguna cadena sugerida. Si el usuario selecciona la opción de búsqueda, la aplicación debe iniciar un motor de búsqueda para ayudar al usuario.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Usar orígenes predefinidos de autocompletar

La finalización automática depende de tener un origen que proporcione cadenas que coincidan con la cadena parcial del usuario. Tiene la opción de proporcionar un origen personalizado de autocompletar, pero el sistema proporciona varios de los orígenes más comunes.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory
</dt> <dd>

Origen de autocompletar que coincide con la lista de direcciones URL en la lista de historial del usuario.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU
</dt> <dd>

Origen de autocompletar que coincide con la lista de direcciones URL en la lista de usuarios usados recientemente.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF
</dt> <dd>

Origen de autocompletar que coincide con los elementos del espacio de nombres del shell: los archivos del equipo del usuario, así como los elementos de las carpetas virtuales como el panel de control.

</dd> </dl>

Hay ocasiones en las que, en lugar de liberar inmediatamente los recursos, es posible que desee conservar los punteros de interfaz en los distintos objetos implicados en Autocompletar. En concreto, esto se hace cuando desea ajustar el comportamiento de autocompletar dinámicamente. La instancia más común de esto se produce cuando se usa el \_ objeto CLSID ACListISF, que se completa de forma autocompleta desde el espacio de nombres del shell y tiene la opción ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) de enumerar también desde el directorio actual. Por ejemplo, cuando se navega a una nueva carpeta, Internet Explorer cambia el directorio actual de la barra de direcciones y, por tanto, la configuración debe cambiarse de forma dinámica. Hay dos maneras de especificar el directorio que el \_ objeto ACLISTISF CLSID debe tratar como el directorio actual:

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) especifica el directorio a través de un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) especifica el directorio a través de una cadena de ruta de acceso.

En los siguientes Supongamos que **PAL** es un puntero a la interfaz [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) de un \_ objeto ACListISF CLSID:

-   Usar [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):

    Para indicar al \_ objeto ACListISF de CLSID que un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) determinado debe tratarse como el directorio actual, puede usar la interfaz [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) del objeto. Dado que un **ITEMIDLIST** puede hacer referencia a una carpeta virtual, este método es más flexible que el uso de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Tenga en cuenta que en los ejemplos siguientes se usa hace plantilla QueryInterface, que permite una lista de parámetros simplificada.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Usar [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):

    Para asignar al \_ objeto CLSID ACListISF una ruta de acceso como directorio actual, puede usar la interfaz [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) del objeto.

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

    

 

 
