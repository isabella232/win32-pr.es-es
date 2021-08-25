---
description: En Windows Vista, el Panel de entrada de Tablet PC integra nuevas funcionalidades de autocompletar que permiten que la lista autocompletar de una aplicación se actualice en tiempo real a medida que se reconoce la entrada de lápiz de un usuario en el Panel de entrada.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Usar autocompletar del panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb0589cca00a45d007c7df6a605f051161c07a62c864504780c307693fe8897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934389"
---
# <a name="using-input-panel-autocomplete"></a>Usar autocompletar del panel de entrada

En Windows Vista, el Panel de entrada de Tablet PC integra nuevas funcionalidades de autocompletar que permiten que la lista autocompletar de una aplicación se actualice en tiempo real a medida que se reconoce la entrada de lápiz de un usuario en el Panel de entrada. Además, la lista Autocompletar de la aplicación se coloca en una ubicación adecuada para los usuarios del Panel de entrada. Sin autocompletar del panel de entrada, el uso de características de autocompletar con el Panel de entrada es un proceso difícil, que requiere que los usuarios inserten un carácter a la vez y muevan el Panel de entrada para acceder a las sugerencias de Autocompletar. Con la integración, Autocompletar es una herramienta eficaz para los usuarios de Tablet PC que acelera y aumenta la facilidad de escribir texto con el Panel de entrada.

![Panel de entrada con la lista de autocompletar](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Hay tres opciones para cómo una aplicación puede aprovechar la integración de autocompletar del panel de entrada. Las aplicaciones que contienen la funcionalidad autocompletar creada mediante Autocompletar de Shell (a través de la interfaz [**IAutoComplete)**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) o .NET Framework Autocompletar (a través de la enumeración [AutoCompleteMode)](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) reciben la integración de autocompletar del panel de entrada sin necesidad de cambios de código. Las aplicaciones que incluyen campos de texto de autocompletar personalizados pueden usar la API autocompletar del panel de entrada para obtener la misma funcionalidad.

En todos los casos, puede realizar estas modificaciones en la lista Autocompletar de la aplicación sin duplicar ni modificar la interfaz de usuario o la lógica de predicción que usa una aplicación para generar una lista de autocompletar. La aplicación sigue dibujando la lista Autocompletar y el contenido de la lista Autocompletar es el mismo que si el texto se hubiera escrito directamente en el campo de edición.

La integración de autocompletar del panel de entrada se admite Windows sistema operativo Vista o versiones posteriores. La integración de autocompletar del panel de entrada se integra en Autocompletar de Shell a partir de Windows Vista y en el desarrollo de Windows Forms a partir .NET Framework versión 3.0. Aunque [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) y [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) se ejecutan en versiones anteriores de Windows, la integración de autocompletar del panel de entrada no se admite en Microsoft Windows XP Tablet PC Edition ni en sistemas operativos anteriores. Si ejecuta Autocompletar del Panel de entrada en versiones anteriores de Tablet PC, las aplicaciones vuelven al comportamiento anterior a la integración.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Motivos para integrar listas de autocompletar de aplicaciones con el panel de entrada

La integración de la lista Autocompletar de una aplicación permite la máxima facilidad y velocidad de entrada para los usuarios que escriben texto en un campo de texto que incluye la funcionalidad autocompletar. Además, una aplicación que incluye la integración de autocompletar del panel de entrada aparece inmediatamente como si se desarrollara pensando en tablet PC, lo que hace que la aplicación sea más atractiva para los usuarios de Tablet PC.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Cómo interactúan el panel de entrada y la lista de autocompletar sin integración

Usar el Panel de entrada para escribir texto en un campo de texto que incluya una lista Autocompletar pero que no esté integrada con el Panel de entrada:

1.  El usuario coloca el foco en el campo de texto y abre el Panel de entrada.
2.  El usuario escribe uno o dos caracteres.
3.  El usuario pulsa **Insertar**. El Panel de entrada escribe el texto en el campo de texto de la aplicación. Aparece la lista Autocompletar de la aplicación y lo más probable es que el Panel de entrada lo oculte parcial o completamente.
4.  El usuario arrastra el Panel de entrada para descubrir la lista Autocompletar de la aplicación.
5.  Suponiendo que la entrada correcta se incluye en la lista Autocompletar, el usuario ahora puede seleccionar esa entrada. De lo contrario, el usuario debe repetir los pasos 2 y 3.

Se trata claramente de un proceso complicado. Las expectativas del usuario sobre cómo debe funcionar una lista de autocompletar están discontinuas y su capacidad para realizar tareas se resfría.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Cómo mejora la interacción del panel de entrada y la lista de autocompletar con la integración

Uso del Panel de entrada para escribir texto en un campo de texto que incluye una lista autocompletar que se integra con el Panel de entrada:

1.  El usuario coloca el foco en el campo de texto y abre el Panel de entrada.
2.  El usuario escribe uno o dos caracteres. La lista Autocompletar de la aplicación aparece directamente encima o directamente debajo del Panel de entrada a medida que el usuario escribe texto.
3.  El usuario selecciona la entrada en la lista Autocompletar; la entrada se inserta directamente en el campo de texto de la aplicación o el usuario repite el paso 2 hasta que aparece la entrada correcta.

Debido a la integración, aparece la lista Autocompletar y se actualiza mientras el usuario escribe en el Panel de entrada. Además, la lista se coloca para que el usuario pueda acceder a ella mientras escribe y no se oculta en el Panel de entrada. Por último, cuando el usuario selecciona un elemento de una lista Autocompletar, el elemento se inserta directamente en el campo de entrada de texto de la aplicación, lo que permite al usuario omitir el paso de insertar texto desde el Panel de entrada.

![Panel de entrada con la lista de autocompletar rápido de Outlook](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Componentes de autocompletar estándar que incluyen la integración de autocompletar del panel de entrada

[**IAutoComplete y**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) [AutoCompleteMode incluyen](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) la integración integrada de Autocompletar del panel de entrada. Las aplicaciones que usan cualquiera de estos componentes estándar de Autocompletar pueden aprovechar la funcionalidad autocompletar del panel de entrada con poco o ningún trabajo adicional. Además, aunque la función Autocompletar del panel de entrada solo se admite en Windows Vista o en nuevas versiones del sistema operativo Windows, las aplicaciones que se crearon con **IAutoComplete** antes del lanzamiento de Windows Vista obtienen la integración de autocompletar del panel de entrada automáticamente cuando se ejecutan en Windows Vista. Las secciones siguientes contienen más información sobre los elementos **IAutoComplete** y AutoCompleteMode específicos que incluyen la integración de autocompletar del panel de entrada.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Autocompletar de Shell con integración de autocompletar del panel de entrada

Las aplicaciones que [**usan IAutoComplete obtienen**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) la integración de autocompletar del panel de entrada de forma gratuita. Aunque las API de autocompletar de Shell se incluyen en Windows 2000 en adelante, la integración de autocompletar del panel de entrada solo es compatible con Windows Vista y versiones más recientes. Sin embargo, las aplicaciones creadas antes del lanzamiento de Windows Vista que usan **IAutoComplete** obtienen automáticamente la integración de autocompletar del panel de entrada cuando se ejecutan en Windows Vista.

Para aprovechar las ventajas de la función Autocompletar de tabletas de esta manera, debe usar el objeto autocompletar **(CLSID \_ Autocompletar).** Si desea proporcionar funcionalidad de autocompletar para direcciones URL o nombres de archivo, use la función [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) para crear el objeto autocompletar.

Además de [**IAutoComplete,**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete)puede implementar [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) o [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)directamente y obtener automáticamente la integración autocompletar del panel de entrada.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Integración de autocompletar del panel de entrada .NET Framework aplicaciones

A partir .NET Framework 3.0, los cuadros de texto Windows Forms incluyen Autocompletar. Windows El cuadro de texto Autocompletar de formularios se basa en Autocompletar del shell, lo que significa que la integración de autocompletar del panel de entrada también está integrada. .NET Framework 3.0 se admite de nivel inferior en Windows ediciones publicadas antes de Windows Vista. Sin embargo, dado que la integración de autocompletar del panel de entrada solo se admite en Windows Vista o versiones posteriores, la integración de autocompletar del panel de entrada solo funciona en una aplicación .NET Framework 3.0 cuando se instala en Windows Vista o versiones posteriores.

Las aplicaciones que desean aprovechar la integración de autocompletar del Panel de entrada en .NET Framework 3.0 deben usar un [textBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) de Windows Forms con la [propiedad AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) habilitada. No es necesario realizar ningún trabajo adicional más allá de obtener Windows Forms Autocompletar para aprovechar las ventajas de la integración de autocompletar del panel de entrada.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Uso de las API de autocompletar del panel de entrada directamente

Los desarrolladores de cuadros de texto autocompletar personalizados deben trabajar con las API autocompletar del panel de entrada directamente para obtener la experiencia de entrada de texto mejorada que la integración de autocompletar del panel de entrada habilita en sus aplicaciones. Las API de autocompletar del panel de entrada se incluyen como parte del sistema operativo Windows Vista y como parte del SDK de tablet platform versión 1.9 o posterior. Las interfaces autocompletar del panel de entrada son interfaces basadas en COM.

En la sección siguiente se describe cómo trabajar estas interfaces en detalle para una aplicación de C++. Sin embargo, estas interfaces COM se pueden implementar en la mayoría de los lenguajes, incluido C \# , mediante el uso de interoperabilidad COM.

Para implementar la integración de autocompletar del Panel de entrada en un cuadro de texto autocompletar personalizado, las dos interfaces necesarias son la interfaz [**ITipAutocompleteProvider**](itipautocompleteprovider.md) y la interfaz [**ITipAutocompleteClient**](itipautocompleteclient.md). Las definiciones de estas interfaces se encuentran en TipAutoComplete.h y TipAutoComplete \_ i.c.

En primer lugar, una aplicación debe definir y crear instancias de una clase de proveedor autocompletar, que implementa [**ITipAutocompleteProvider para**](itipautocompleteprovider.md) cada campo de entrada de texto que incluya una lista de autocompletar. Esta clase administra el lado de la aplicación de la integración de autocompletar. Todas las solicitudes de autocompletar del Panel de entrada se realizan desde el cliente autocompletar a la aplicación a través del proveedor autocompletar de la aplicación. El proveedor de autocompletar de la aplicación debe tener acceso al HWND de la lista Autocompletar de la aplicación y al HWIND para el campo de entrada de texto asociado. Además, se deben implementar los métodos siguientes de **ITipAutocompleteProvider:**

-   [**ITipAutocompleteProvider::UpdatePendingText (Método):**](itipautocompleteprovider-updatependingtext.md)el cliente de Autocomplete usa este método para notificar a la aplicación el texto que un usuario ha escrito en el Panel de entrada. Tras recibir esta notificación, el proveedor es responsable de generar una lista de autocompletar como si el texto se hubiera escrito en el campo de entrada de texto de la aplicación. La cadena pasa al proveedor autocompletar mediante el método **ITipAutocompleteProvider::UpdatePendingText solo** incluye el texto actualmente en el Panel de entrada. Por lo tanto, si hay texto adicional en el campo de entrada de texto, es responsabilidad del proveedor anexar correctamente al texto enviado por el cliente. La cadena pasada por el método **ITipAutocompleteProvider::UpdatePendingText** debe tratarse como un reemplazo de la selección actual en el campo. Si no hay ninguna selección actual, debe colocarse en la posición del punto de inserción actual. Una vez generada la lista Autocompletar, el proveedor debe llamar al método [**ITipAutocompleteProvider::Show**](itipautocompleteprovider-show.md) pasando **TRUE** para mostrar la lista Autocompletar. La aplicación no debe almacenar en caché las llamadas a **UpdatePendingText,** sino tratar cada llamada adicional a **UpdatePendingText** como una cancelación de la llamada anterior para evitar que se parpadee una interfaz de usuario de lista de autocompletar no actualizada. En el código de ejemplo siguiente se ilustran estas prácticas.

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

    

-   [**ITipAutocompleteProvider::Show (Método):**](itipautocompleteprovider-show.md)se llama a este método desde [**UpdatePendingText,**](itipautocompleteprovider-updatependingtext.md)pero el cliente autocompletar también puede llamar a este método en cualquier momento. Tras recibir esta llamada, el proveedor de autocompletar debe ocultar o mostrar el proveedor autocompletar tal y como indica el parámetro . Antes de mostrar la lista Autocompletar, se espera que el proveedor de Autocompletar consulte al cliente autocompletar sobre dónde colocar la lista Autocompletar. Más información sobre cómo colocar la lista Autocompletar aparece más adelante en este artículo.

A continuación, la aplicación debe usar la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) de Active Template Library (ATL) para generar una instancia de la interfaz [**ITipAutocompleteClient**](itipautocompleteclient.md) con el identificador de clase **CLSID \_ TipAutoCompleteClient** como servidor en proceso y, a continuación, registrar el proveedor con el cliente. El método [**ITipAutocompleteClient::AdviseProvider**](itipautocompleteclient-adviseprovider.md) del cliente autocompletar registra el proveedor con el cliente para permitir que el cliente llame al objeto del proveedor autocompletar de la aplicación. Si tiptsf.dll está presente en el sistema, se produce un error en la función **CoCreateInstance** y devuelve **REGDB \_ E \_ CLASSNOTREG**. En este momento, la aplicación puede descartar su objeto [**ITipAutocompleteProvider**](itipautocompleteprovider.md) y continuar como si el Panel de entrada no existiera, porque no existe en dicho sistema.

La aplicación puede optar por crear una instancia de [**ITipAutocompleteClient**](itipautocompleteclient.md) o una instancia por campo de texto. La primera opción requiere que el proveedor se anulará del registro y se registrará cada vez que se cambie el foco. Más adelante en este tema se muestra más información sobre cómo anular el registro del proveedor de autocompletar.

Hay varios pasos implicados en la colocación de la lista autocompletar que deben coordinarse entre el proveedor de autocompletar (aplicación) y el cliente autocompletar (panel de entrada). Antes de que se muestre la lista Autocompletar, ya sea como resultado de una llamada al método [**Show**](itipautocompleteprovider-show.md) del proveedor de Autocompletar o debido a que el usuario escribe texto mediante el teclado, se requiere que el proveedor consulte al cliente sobre dónde colocar la lista Autocompletar. El proveedor debe realizar los pasos siguientes:

-   Use el método [**ITipAutocompleteClient::RequestShowUI**](itipautocompleteclient-requestshowui.md) del cliente autocompletar para determinar si el Panel de entrada está listo para mostrar la lista Autocompletar. **RequestShowUI** toma el *parámetro HWND* que es el HWND de la ventana de lista Autocompletar y el método devuelve **TRUE** o **FALSE** para indicar si es el estado en el que se puede mostrar la lista Autocompletar. Si el cliente devuelve **FALSE**, el proveedor no debe intentar mostrar la lista Autocompletar.
-   Llame [**a RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer el identificador de ventana de lista de autocompletar emergente antes de llamar al método [**ITipAutocompleteClient::P referredRects**](itipautocompleteclient-preferredrects.md). Si no lo hace, se producirá un error **E \_ INVALIDARG** al llamar a **PreferredRects**.
-   Si [**RequestShowUI**](itipautocompleteclient-requestshowui.md) devuelve **TRUE,** el proveedor debe calcular el rectángulo de coordenadas de pantalla predeterminado de la lista autocompletar en función de la ubicación del campo de entrada de texto y, a continuación, llamar al método [**ITipAutocompleteClient::P referredRects del**](itipautocompleteclient-preferredrects.md)cliente autocompletar . Esto permite que el cliente autocompletar ajuste el rectángulo para evitar que la lista autocompletar se superponga con el Panel de entrada. El **método PreferredRects** toma cuatro parámetros:

    -   RECT *rcACList:* rectángulo de coordenadas de pantalla predeterminado de la lista Autocompletar.
    -   RECT *rcField:* rectángulo de coordenadas de pantalla del campo de entrada de texto correspondiente.
    -   RECT *\* prcModifiedACList:* rectángulo de coordenadas de pantalla ajustado para autocompletar
    -   BOOL *\* pfShowAbove:* este parámetro indica al proveedor si el rectángulo *prcModifiedACList* coloca la lista Autocompletar encima o debajo del Panel de entrada. La aplicación puede usar esta información para dibujar correctamente elementos de la interfaz de usuario, como identificadores de cambio de tamaño y barras de desplazamiento. Inicialmente, el proveedor debe pasar en la dirección en la que *rcACList* colocaría la lista autocompletar en relación con el campo de entrada de texto. El cliente no cambia *pfShowAbove si* establece *prcModifiedACList igual* a *rcACList*.

    Use los valores devueltos de los argumentos *prcModifiedACList* y *pfShowAbove* out para colocar y mostrar la ventana de lista Autocompletar. Si el Panel de entrada no está en uso, [**RequestShowUI**](itipautocompleteclient-requestshowui.md) siempre devuelve **TRUE** y *prcModifiedACList* siempre es el mismo que *rcACList.* *pfShowAbove* tampoco se modifica; el resultado es que las llamadas no tienen ningún efecto en el comportamiento de la aplicación. En el código de ejemplo siguiente se ilustran estas prácticas.


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



Cuando el usuario selecciona un elemento en la lista Autocompletar, el proveedor debe llamar al método [**ITipAutocompleteClient::UserSelection**](itipautocompleteclient-userselection.md) del cliente, además de insertar el texto del elemento seleccionado en el campo de entrada de texto. El Panel de entrada usa esta notificación para descartar todo el texto restante que aún no se ha insertado desde el Panel de entrada.

Por último, cuando el proveedor ya no sea necesario, el proveedor debe desvincularse del cliente autocompletar llamando al método [**ITipAutocompleteClient::UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) del cliente autocompletar para anular el registro del proveedor. Es posible que sea necesario anular el registro del proveedor por uno de estos dos motivos: porque se ha destruido el campo de entrada de texto al que está asociado el proveedor o porque la aplicación decide crear solo un cliente autocompletar, en lugar de uno por cada campo de entrada de texto. En este caso, el proveedor debe anularse del registro cada vez que el foco se desconecte del campo de texto.

## <a name="conclusion"></a>Conclusión

La integración de autocompletar del panel de entrada es una herramienta eficaz para mejorar la experiencia del usuario en Windows aplicaciones que incluyen listas de autocompletar en equipos tablet. Sin la integración, los usuarios del Panel de entrada deben pasar por un tedioso proceso de insertar texto de un carácter a la vez y cambiar la posición del Panel de entrada para poder usar autocompletar. Con la integración, las listas de autocompletar aparecen en una ubicación cómoda a medida que los usuarios se insinutan en el Panel de entrada, lo que aumenta la velocidad y la facilidad de entrada de texto. En las aplicaciones que incluyen la funcionalidad autocompletar integrada en Autocompletar de Shell o autocompletar de .NET Framework 3.0, la integración de autocompletar del panel de entrada es una característica gratuita y atractiva. Además, se proporciona un conjunto sencillo de interfaces basadas en COM para habilitar la misma experiencia integrada para las aplicaciones que deciden usar controles de autocompletar personalizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 
