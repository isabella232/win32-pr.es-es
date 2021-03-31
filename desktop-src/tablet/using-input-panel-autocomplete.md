---
description: En Windows Vista, el panel de entrada de Tablet PC integra nuevas capacidades de autocompletar que permiten que la lista de autocompletar de una aplicación se actualice en tiempo real a medida que se reconoce la tinta de un usuario en el panel de entrada.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Uso de autocompletar del panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e7f108631eb2723b71bf8ed919c17a0eabff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154184"
---
# <a name="using-input-panel-autocomplete"></a>Uso de autocompletar del panel de entrada

En Windows Vista, el panel de entrada de Tablet PC integra nuevas capacidades de autocompletar que permiten que la lista de autocompletar de una aplicación se actualice en tiempo real a medida que se reconoce la tinta de un usuario en el panel de entrada. Además, la lista de autocompletar de la aplicación se coloca en una ubicación adecuada para los usuarios del panel de entrada. Sin la función autocompletar del panel de entrada, el uso de las características de autocompletar con el panel de entrada es un proceso difícil, que requiere que los usuarios inserten un carácter cada vez y muevan el panel de entrada para obtener acceso a las sugerencias de autocompletar. Con la integración, Autocompletar es una herramienta eficaz para los usuarios de Tablet PC que acelera y aumenta la facilidad de escribir texto con el panel de entrada.

![panel de entrada con la lista de autocompletar de IE](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Hay tres opciones para la forma en que una aplicación puede aprovechar la integración de autocompletar del panel de entrada. Las aplicaciones que contienen la funcionalidad Autocompletar compilada con el autocompletar de Shell (a través de la interfaz [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) ) o .NET Framework autocompletar (a través de la enumeración [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) ) reciben la integración de autocompletar del panel de entrada sin necesidad de realizar cambios en el código Las aplicaciones que incluyen campos de texto de autocompletar personalizados pueden usar la API Autocompletar del panel de entrada para obtener la misma funcionalidad.

En todos los casos, puede realizar estas modificaciones en la lista de autocompletar de la aplicación sin duplicar ni modificar la interfaz de usuario o la lógica de predicción usada por una aplicación para generar una lista de autocompletar. La lista Autocompletar sigue siendo propietaria de la aplicación y el contenido de la lista Autocompletar es el mismo que si el texto se hubiera escrito directamente en el campo de edición.

La integración de autocompletar del panel de entrada es compatible con el sistema operativo Windows Vista o versiones posteriores. La integración de autocompletar del panel de entrada está integrada en Shell Autocompletar a partir de Windows Vista y en Windows Forms desarrollo a partir de .NET Framework versión 3,0. Aunque [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) y [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) se ejecutan en versiones anteriores de Windows, la integración de autocompletar del panel de entrada no es compatible con Microsoft Windows XP Tablet PC Edition ni con sistemas operativos anteriores. Si ejecuta la función autocompletar del panel de entrada en versiones anteriores de Tablet PC, las aplicaciones volverán al comportamiento de la integración previa.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Razones para integrar las listas de autocompletar de aplicaciones con el panel de entrada

La integración de la lista de autocompletar de una aplicación permite la facilidad y la velocidad máximas de entrada para los usuarios que escriben texto en un campo de texto que incluye la funcionalidad de autocompletar. Además, una aplicación que incluye la integración de autocompletar panel de entrada aparece inmediatamente como si se hubiera desarrollado con Tablet PC en mente, lo que dificulta a los usuarios de Tablet PC.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Cómo interactúa el panel de entrada y la lista Autocompletar sin integración

Usar el panel de entrada para escribir texto en un campo de texto que incluye una lista de autocompletar, pero que no está integrado con el panel de entrada:

1.  El usuario coloca el foco en el campo de texto y abre el panel de entrada.
2.  El usuario escribe uno o dos caracteres.
3.  El usuario puntea **Insertar**. El panel de entrada escribe el texto en el campo de texto de la aplicación. La lista autocompletar de la aplicación aparece y es más probable parcialmente o totalmente oculta por el panel de entrada.
4.  El usuario arrastra el panel de entrada para descubrir la lista de autocompletar de la aplicación.
5.  Suponiendo que la entrada correcta está incluida en la lista Autocompletar, el usuario puede seleccionar la entrada. de lo contrario, el usuario debe repetir los pasos 2 y 3.

Este proceso es claramente complicado. Las expectativas del usuario de cómo funciona una lista de autocompletar se desaconsejan y su capacidad para realizar tareas se ve afectada.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Cómo mejora la interacción del panel de entrada y la lista de autocompletar con la integración

Usar el panel de entrada para escribir texto en un campo de texto que incluye una lista de autocompletar que se integra con el panel de entrada:

1.  El usuario coloca el foco en el campo de texto y abre el panel de entrada.
2.  El usuario escribe uno o dos caracteres. La lista autocompletar de la aplicación aparece directamente encima o justo debajo del panel de entrada cuando el usuario escribe texto.
3.  El usuario selecciona la entrada de la lista Autocompletar; la entrada se inserta directamente en el campo de texto de la aplicación o el usuario repite el paso 2 hasta que aparezca la entrada correcta.

Debido a la integración, la lista Autocompletar aparece y se actualiza mientras el usuario escribe en el panel de entrada. Además, la lista se coloca para que sea conveniente que el usuario tenga acceso a ella y no esté oculta por el panel de entrada. Por último, cuando el usuario selecciona un elemento de una lista de autocompletar, el elemento se inserta directamente en el campo de entrada de texto de la aplicación, lo que permite al usuario omitir el paso de insertar texto del panel de entrada.

![panel de entrada con la lista autocompletar de Outlook Express](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Componentes de autocompleta estándar que incluyen la integración de autocompletar del panel de entrada

Tanto [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) como [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) incluyen integración integrada de autocompletar del panel de entrada. Las aplicaciones que usan cualquiera de estos componentes de autocompleta estándar pueden aprovechar la funcionalidad de autocompletar del panel de entrada con poco o ningún trabajo adicional. Además, aunque la función autocompletar del panel de entrada solo se admite en Windows Vista o en las versiones nuevas del sistema operativo Windows, las aplicaciones que se crearon con **IAutoComplete** antes del lanzamiento de Windows Vista obtienen la integración de autocompletar del panel de entrada automáticamente cuando se ejecutan en Windows Vista. En las secciones siguientes se incluye más información sobre los elementos **IAutoComplete** y AutoCompleteMode específicos que incluyen la integración de autocompletar del panel de entrada.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Autocompletar Shell con la integración de autocompletar del panel de entrada

Las aplicaciones que usan [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) obtienen la integración de autocompletar del panel de entrada de forma gratuita. Aunque las API de autocompletar Shell se incluyen en Windows 2000, la integración de autocompletar del panel de entrada solo es compatible con Windows Vista y versiones más recientes. Sin embargo, las aplicaciones compiladas antes del lanzamiento de Windows Vista que usan **IAutoComplete** automáticamente obtienen la integración de autocompletar del panel de entrada cuando se ejecutan en Windows Vista.

Con el fin de aprovechar la función autocompletar de Tablet PC de esta manera, debe usar el objeto autocompletar (**CLSID \_ AutoComplete**). Si desea proporcionar funcionalidad de Autocompletar para direcciones URL o nombres de archivo, use la función [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) para crear el objeto Autocompletar.

Además de [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete), puede implementar [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) o [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)s directamente y seguir con la integración automática del panel de entrada automáticamente.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Integración de autocompletar del panel de entrada con .NET Framework aplicaciones

A partir de .NET Framework 3,0, Windows Forms cuadros de texto incluyen Autocompletar. Windows Forms Autocompletar TextBox se basa en Autocompletar Shell, lo que significa que también se integra la integración de autocompletar del panel de entrada. .NET Framework 3,0 es compatible con el nivel inferior en las ediciones de Windows publicadas antes de Windows Vista. Sin embargo, dado que la integración de autocompletar del panel de entrada solo se admite en Windows Vista o versiones posteriores, la integración de autocompletar del panel de entrada solo funciona en una aplicación .NET Framework 3,0 cuando se instala en Windows Vista o versiones posteriores.

Las aplicaciones que quieran aprovechar la integración de autocompletar del panel de entrada en .NET Framework 3,0 deben usar un [cuadro de texto](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) Windows Forms con la propiedad [AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) habilitada. No es necesario realizar ningún trabajo adicional más allá de obtener Windows Forms Autocompletar para trabajar con el fin de aprovechar la integración de autocompletar del panel de entrada.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Uso de las API de autocompletar del panel de entrada directamente

Los desarrolladores de cuadros de texto de autocompletar personalizados deben trabajar directamente con las API de autocompletar del panel de entrada para obtener la mejor experiencia de entrada de texto que habilita la integración de autocompletar del panel de entrada en sus aplicaciones. Las API de autocompletar del panel de entrada se incluyen como parte del sistema operativo Windows Vista y como parte de la versión 1,9 o posterior del SDK de la plataforma de tableta. Las interfaces de autocompletar del panel de entrada son interfaces basadas en COM.

En la siguiente sección se describe cómo trabajar con estas interfaces en detalle para una aplicación de C++. Sin embargo, estas interfaces COM se pueden implementar en la mayoría de los lenguajes, incluido C \# , mediante el uso de la interoperabilidad com.

Para implementar la integración de autocompletar del panel de entrada en un cuadro de texto de autocompletar personalizado, las dos interfaces necesarias son la [**interfaz ITipAutocompleteProvider**](itipautocompleteprovider.md) y la [**interfaz ITipAutocompleteClient**](itipautocompleteclient.md). Las definiciones de estas interfaces se encuentran en TipAutoComplete. h y TipAutoComplete \_ i.c.

En primer lugar, una aplicación debe definir y crear una instancia de una clase de proveedor de autocompletar, que implementa [**ITipAutocompleteProvider**](itipautocompleteprovider.md) para cada campo de entrada de texto que incluye una lista de autocompletar. Esta clase administra el lado de la aplicación de la integración de autocompletar. Todas las solicitudes de autocompletar del panel de entrada se realizan desde el cliente de autocompletar a la aplicación a través del proveedor de autocompletar de la aplicación. El proveedor de autocompletar de la aplicación debe tener acceso al HWND de la lista de autocompletar de la aplicación y HWIND para el campo de entrada de texto asociado. Además, se deben implementar los siguientes métodos de **ITipAutocompleteProvider** :

-   [**ITipAutocompleteProvider:: UpdatePendingText método**](itipautocompleteprovider-updatependingtext.md): este método lo usa el cliente de Autocompletar para notificar a la aplicación el texto que un usuario ha escrito en el panel de entrada. Tras recibir esta notificación, el proveedor es responsable de generar una lista de autocompletar como si el texto se hubiera escrito en el campo de entrada de texto de la aplicación. La cadena que se pasa al proveedor de autocompletar mediante el **método ITipAutocompleteProvider:: UpdatePendingText** solo incluye el texto que se encuentra actualmente en el panel de entrada. Por lo tanto, si hay texto adicional en el campo de entrada de texto, es responsabilidad del proveedor anexarlo correctamente al texto enviado por el cliente. La cadena pasada por el **método ITipAutocompleteProvider:: UpdatePendingText** se debe tratar como un reemplazo para la selección actual en el campo. Si no hay ninguna selección actual, debe colocarse en la posición del punto de inserción actual. Una vez que se genera la lista de autocompletar, el proveedor debe llamar al [**método ITipAutocompleteProvider:: show**](itipautocompleteprovider-show.md) pasando **true** para mostrar la lista de autocompletar. La aplicación no debe almacenar en caché las llamadas a **UpdatePendingText** , sino tratar cada llamada adicional a **UpdatePendingText** como una cancelación de la llamada anterior para evitar la intermitencia de una interfaz de usuario de lista de autocompletar no actualizada. En el ejemplo de código siguiente se muestran estos procedimientos.

    ```C++
    HRESULT SampleProvider::UpdatePendingText(BSTR bstrPendingText)
    {
       //Discard previously cached pending text from Input Panel
       m_bstrPending.Empty();
        //Store the new pending text from Input Panel as m_bstrPending
    m_bstrPending = bstrPendingText;

        //Get the text from the field in two chunks. The characters to
    //the left of the selection and the characters to the right.
    CComBSTR bstrLeftContext = //Text to the left of the selection
            CComBSTR bstrRightContext = //Text to the right of the selection

    //Discard previously cached complete text
        m_bstrCompleteText.Empty();
        //Append to the field text from the left of the selection
        //the text from Input Panel and then append to that
        //the field text to the right of the selection
        m_bstrCompleteText.Append(bstrLeftContext);
        m_bstrCompleteText.Append(m_bstrPending);
        m_bstrCompleteText.Append(bstrRigtContext);

        //Update the app's AC list based on m_bstrCompleteText
        //...

        //Show the updated AC list by calling the provider's Show method
       Show(true);
       return S_OK;
    }
    ```

    

-   [**ITipAutocompleteProvider:: show Method**](itipautocompleteprovider-show.md): este método se llama desde [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md), pero el cliente de autocompletar también puede llamarlo en cualquier momento. Al recibir esta llamada, el proveedor de autocompletar debe ocultar o mostrar el proveedor de autocompletar tal y como se indica en el parámetro. Antes de mostrar la lista de autocompletar, se espera que el proveedor de autocompletar consulte al cliente de autocompletar dónde se debe colocar la lista de autocompletar. Más adelante en este artículo encontrará más información sobre cómo colocar la lista Autocompletar.

A continuación, la aplicación debe usar la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) de Active Template Library (ATL) para generar una instancia de la [**interfaz ITipAutocompleteClient**](itipautocompleteclient.md) con ID. de clase **CLSID \_ TipAutoCompleteClient** como un servidor en proceso y, a continuación, registrar el proveedor con el cliente. El [**método ITipAutocompleteClient:: AdviseProvider**](itipautocompleteclient-adviseprovider.md) del cliente Autocompletar registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación. Si tiptsf.dll no está presente en el sistema, se produce un error en la función **CoCreateInstance** y se devuelve **REGDB \_ e \_ CLASSNOTREG**. En este punto, la aplicación puede descartar su objeto [**ITipAutocompleteProvider**](itipautocompleteprovider.md) y continuar como si no existiera el panel de entrada, porque no se encuentra en ese sistema.

La aplicación puede optar por crear una instancia de [**ITipAutocompleteClient**](itipautocompleteclient.md) o una instancia por cada campo de texto. La primera opción requiere que se anule el registro del proveedor y se registre cada vez que se cambie el foco. Más adelante en este tema se muestra más información sobre cómo anular el registro del proveedor de autocompletar.

Hay varios pasos que deben seguirse para colocar la lista Autocompletar que debe coordinarse entre el proveedor de autocompletar (aplicación) y el cliente de autocompletar (panel de entrada). Antes de que se muestre la lista Autocompletar, ya sea como resultado de una llamada al método [**Show**](itipautocompleteprovider-show.md) del proveedor de autocompletar o debido a que el usuario escribe texto con el teclado, el proveedor debe consultar al cliente dónde debe colocar la lista de autocompletar. El proveedor debe llevar a cabo los siguientes pasos:

-   Use el [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) del cliente de Autocompletar para determinar si el panel de entrada está listo para mostrar la lista Autocompletar. **RequestShowUI** toma el parámetro *hWnd* , que es el HWND de la ventana Lista de autocompletar, y el método devuelve **true** o **false** para indicar si es el estado en el que se puede mostrar la lista Autocompletar. Si el cliente devuelve **false**, el proveedor no debe intentar Mostrar la lista de autocompletar.
-   Llame a [**RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer el identificador de la ventana de lista de autocompletar emergente antes de llamar al [**método referredrects de ITipAutocompleteClient::P**](itipautocompleteclient-preferredrects.md). Si no lo hace, se producirá un error de **E \_ INVALIDARG** al llamar a **PreferredRects**.
-   Si [**RequestShowUI**](itipautocompleteclient-requestshowui.md) devuelve **true**, el proveedor debe calcular el rectángulo de coordenadas de pantalla predeterminado de la lista autocompletar en función de la ubicación del campo de entrada de texto y, a continuación, llamar al [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md)de cliente de autocompletar. Esto permite al cliente Autocompletar ajustar el rectángulo para evitar que la lista Autocompletar se superponga con el panel de entrada. El método **PreferredRects** toma cuatro parámetros:

    -   RECT *rcACList*: el rectángulo de coordenadas de pantalla predeterminado de la lista de autocompletar.
    -   RECT *rcField*: el rectángulo de coordenadas de la pantalla del campo de entrada de texto correspondiente.
    -   RECT *\* prcModifiedACList*: el rectángulo de coordenadas de pantalla ajustado para Autocompletar
    -   BOOL *\* pfShowAbove*: este parámetro indica al proveedor si el rectángulo *prcModifiedACList* coloca la lista Autocompletar por encima o por debajo del panel de entrada. La aplicación puede usar esta información para dibujar correctamente los elementos de la interfaz de usuario, como los controladores de tamaño y las barras de desplazamiento. El proveedor debe pasar inicialmente la dirección en la que se colocará la lista autocompletar en relación con el campo de entrada de texto *rcACList*. El cliente no cambia *pfShowAbove* si establece *PrcModifiedACList* igual a *rcACList*.

    Use los valores devueltos de los argumentos *prcModifiedACList* y *pfShowAbove* out para colocar y mostrar la ventana Lista de autocompletar. Si el panel de entrada no está en uso, [**RequestShowUI**](itipautocompleteclient-requestshowui.md) siempre devuelve **true** y *PrcModifiedACList* siempre es igual que *rcACList*. *pfShowAbove* también es inalterado, el resultado es que las llamadas no tienen ningún efecto en el comportamiento de la aplicación. En el ejemplo de código siguiente se muestran estos procedimientos.


```C++
HRESULT SampleProvider::Show(BOOL fShow)
{
    //Ask the AC client if it is OK to show the Autocomplete list.
    BOOL fAllowShowing = FALSE;
    m_spACClient->RequestShowUI(m_hWndList, &fAllowShowing);

    if (fShow && fAllowingShowing)
        {
            // Create the parameters required to call PreferredRects
            RECT rcField = //Rectangle for app's text field
            RECT rcACList = //Default rectangle for app's AC list
            RECT rcModifiedACList = {0, 0, 0, 0};
            BOOL fShowAbove = TRUE;

//Ask the AC client to modify the position of the AC list
m_spACClient->PreferredRects(&rcACList, &rcField,
&rcModifiedACList, &fShowAbove);

            //Show the Autocomplete UI at the modified preferred rectangle
            //from rcModifiedACList and the directional info provide by
//fShowAbove
            //...
        }
    else
        {
        //Hide the Autocomplete list and clean up
        //...
        }
    return S_OK;
}
```



Cuando el usuario selecciona un elemento en la lista Autocompletar, el proveedor debe llamar al [**método ITipAutocompleteClient:: UserSelection**](itipautocompleteclient-userselection.md) del cliente además de insertar el texto del elemento seleccionado en el campo de entrada de texto. El panel de entrada utiliza esta notificación para descartar todo el texto restante que todavía no se ha insertado en el panel de entrada.

Por último, cuando el proveedor ya no es necesario, se debe desvincular el proveedor del cliente de autocompletar llamando al [**método ITipAutocompleteClient:: UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) del cliente de Autocompletar para anular el registro del proveedor. Puede que sea necesario anular el registro del proveedor por uno de estos dos motivos: porque el campo de entrada de texto al que está asociado el proveedor se ha destruido, o porque la aplicación elige crear solo un cliente de autocompletar, en lugar de uno por cada campo de entrada de texto. En esta instancia, se debe anular el registro del proveedor cada vez que el foco se salga del campo de texto.

## <a name="conclusion"></a>Conclusión

La integración de autocompletar del panel de entrada es una herramienta eficaz para mejorar la experiencia del usuario en aplicaciones de Windows que incluyen listas de autocompletar en Tablet PC. Sin la integración de, los usuarios del panel de entrada tienen que pasar por un proceso tedioso de insertar texto en carácter en cada momento y cambiar la posición del panel de entrada para poder usar Autocompletar. Con la integración, las listas de autocompletar aparecen en una ubicación adecuada a medida que los usuarios se escriben en el panel de entrada, lo que aumenta la velocidad y la facilidad de entrada de texto. En las aplicaciones que incluyen la funcionalidad de autocompletar que se basa en autocompletar de shell o .NET Framework 3,0 Autocompletar, la integración de autocompletar de panel de entrada es una característica gratuita y atractiva. Además, se proporciona un conjunto sencillo de interfaces basadas en COM para habilitar la misma experiencia integrada para las aplicaciones que eligen usar controles personalizados de autocompletar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 
