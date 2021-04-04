---
title: Hojas de propiedades de Active Directory usuarios y equipos
description: El complemento de MMC usuarios y equipos de Active Directory está diseñado para mostrar una hoja de propiedades de varios objetos en un servidor de Active Directory.
ms.assetid: 38032d89-9549-475c-90aa-dac5cfe11084
ms.tgt_platform: multiple
keywords:
- Active Directory de las hojas de propiedades usuarios y equipos en AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea24f34e86f21af178e975852accb667bb69e4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789651"
---
# <a name="active-directory-users-and-computers-property-sheets"></a>Hojas de propiedades de Active Directory usuarios y equipos

El complemento de MMC usuarios y equipos de Active Directory está diseñado para mostrar una hoja de propiedades de varios objetos en un servidor de Active Directory. La hoja de propiedades contiene una o varias páginas que se usan para ver y modificar los datos del objeto. Se muestran diferentes conjuntos de páginas para los distintos tipos de objeto. El complemento MMC usuarios y equipos de Active Directory también permite a los proveedores de terceros agregar páginas personalizadas a la hoja de propiedades de un tipo específico de objeto. Para obtener más información, vea [páginas de propiedades para su uso con especificadores de presentación](property-pages-for-use-with-display-specifiers.md).

Algunas aplicaciones, a excepción del complemento MMC de usuarios y equipos de Active Directory, deben proporcionar al usuario la posibilidad de ver y editar los atributos de un objeto en un servidor Active Directory. La aplicación podría implementar sus propias hojas de propiedades, pero es mejor ofrecer una interfaz de usuario coherente para reducir la confusión y el tiempo de aprendizaje. Afortunadamente, el complemento de MMC usuarios y equipos de Active Directory permite que cualquier aplicación OLE COM muestre una hoja de propiedades para un objeto que es idéntica a la hoja de propiedades que se mostraría en el complemento MMC usuarios y equipos del Active Directory para el mismo objeto.

Para obtener más información y un ejemplo de código que hospede una Active Directory hoja de propiedades usuarios y equipos, vea el ejemplo PropSheetHost en el kit de desarrollo de software (SDK) de la plataforma.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

En esta documentación se supone que el lector está familiarizado con el funcionamiento COM y el desarrollo de componentes mediante C++. Actualmente, no es posible crear una extensión de hoja de propiedades Active Directory mediante Visual Basic.

## <a name="hosting-an-active-directory-users-and-computers-property-sheet"></a>Hospedaje de una Active Directory hoja de propiedades usuarios y equipos

**Para mostrar una hoja de propiedades de un objeto en un servidor de Active Directory**

1.  Crea una ventana que se puede usar para procesar mensajes. Puede tratarse de una ventana existente o una ventana de propósito especial. Esto se conoce como la *ventana oculta*.
2.  Cree un objeto OLE COM que se derive de [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject). Este objeto de datos debe admitir los siguientes formatos de datos:

    -   [**CFSTR \_ DSOBJECTNAMES**](cfstr-dsobjectnames.md) este formato de datos contiene un [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que identifica el objeto al que se aplica la hoja de propiedades. Al hospedar una hoja de propiedades, los miembros más significativos de la estructura **DSOBJECTNAMES** se muestran en la lista siguiente.

        **clsidNamespace** Sector. Establezca este valor en un GUID para la aplicación en caso de que se use en el futuro.
        
        **aObjects** Contiene una matriz de estructuras [**DSBOJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Cada estructura **DSBOJECT** representa un objeto de directorio único. El miembro **cItems** contiene el número de elementos de la matriz. Solo se usa el primer objeto de esta matriz. Se omiten otros objetos.

    -   [**CFSTR \_ DSDISPLAYSPECOPTIONS**](cfstr-ds-display-spec-options.md) este formato de datos contiene una estructura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) que contiene los datos que usarán las páginas de propiedades, como dónde cargar las páginas de propiedades, el servidor y las credenciales que se van a usar, etc. Los miembros más importantes de **DSDISPLAYSPECOPTIONS** se muestran en la lista siguiente.

        **offsetAttribPrefix** La cadena de prefijo de atributo determina dónde se obtiene la lista de páginas de propiedades. Debe contener una de las siguientes cadenas.

        

        | Cadena de prefijo de atributo | Descripción                                              |
        |-------------------------|----------------------------------------------------------------------------------------------------------------------|
        | administrar<br/>      | Las páginas de propiedades se cargan desde el atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) .<br/> |
        | interfaz<br/>      | Las páginas de propiedades se cargan desde el atributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) .<br/> |

        


    -   [**CFSTR \_ \_PROPSHEETCONFIG DS**](cfstr-ds-propsheetconfig.md) este formato de datos contiene una estructura [**PROPSHEETCFG**](propsheetcfg.md) que contiene los datos del host de la hoja de propiedades. Al hospedar una hoja de propiedades, los miembros más significativos de la estructura **PROPSHEETCFG** contienen los datos que se muestran en la lista siguiente.

        **lNotifyHandle** Debe ser cero.
        **hwndParentSheet**  Contiene el identificador de la ventana para recibir mensajes de [**\_ cambio de \_ notificación \_ de WM ADSPROP**](wm-adsprop-notify-change.md) cuando se cambia algo en una de las páginas y se aplica. Puede ser **null** si no se desea este mensaje.

        **hwndHidden** Contiene el identificador de la ventana para recibir los mensajes de notificación de la hoja de DSA de WM de la [**\_ creación de \_ \_ \_ notificaciones**](wm-dsa-sheet-create-notify.md) y de la [**\_ \_ hoja \_ \_ DSA de WM**](wm-dsa-sheet-close-notify.md) . Establézcalo en el identificador de la ventana oculta.

        **wParamSheetClose** Contiene un identificador definido por la aplicación que se devuelve en el *wParam* en el mensaje de notificación de cierre de la [**\_ \_ hoja \_ \_ DSA de WM**](wm-dsa-sheet-close-notify.md) . Si este miembro es cero, el mensaje de notificación de cierre de la hoja del DSA de WM no se publicará en la ventana oculta. **\_ \_ \_ \_**


3.  Cree una instancia del objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) y obtenga la interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para el objeto. También es posible duplicar el comportamiento del objeto **\_ DsPropertyPages de CLSID** . Para obtener más información, vea duplicar el comportamiento del \_ objeto DsPropertyPages de CLSID.
4.  Inicialice el objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) llamando al método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . Los parámetros *pidlFolder* y *hkeyProgID* no se usan en este método. El parámetro *pdtobj* es el puntero al objeto de datos creado en el paso 2. Cuando se llama al método **IShellExtInit:: Initialize** , el **objeto \_ DsPropertyPages de CLSID** guardará una referencia al objeto de datos.
5.  Obtenga la interfaz [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) para el [**objeto \_ DsPropertyPages de CLSID**](guids-of-user-interface-elements.md) y llame al método [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . El parámetro *lpfnAddPage* es la dirección de una función de devolución de llamada que se debe implementar. A continuación se muestra el formato de esta función. Si la función de devolución de llamada se declara como un miembro de una clase de C++, la función de devolución de llamada se debe declarar como **estática**. El parámetro *lParam* es un valor definido por la aplicación que se puede utilizar para identificar el objeto que implementa la función de devolución de llamada. Cuando se llama al método **IShellPropSheetExt:: AddPages** , el **objeto \_ DsPropertyPages de CLSID** obtendrá los datos del objeto de datos y enumerará las páginas de propiedades registradas para los especificadores de presentación de objetos. El objeto **CLSID \_ DsPropertyPages** enumerará los objetos de la página de propiedades, llamando al método **IShellPropSheetExt:: AddPages** de cada objeto.

    ```C++
    BOOL CALLBACK AddPagesCallback(HPROPSHEETPAGE, LPARAM)
    ```

    

6.  Cada página agregada por los objetos de la página de propiedades dará como resultado la llamada a la función de devolución de llamada con el identificador de la página de propiedades y el valor definido por la aplicación. La función de devolución de llamada debe almacenar cada identificador de página de propiedades que se pasa. Cuando el método [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) del objeto [**\_ DsPropertyPages CLSID**](guids-of-user-interface-elements.md) devuelva, se agregarán todas las páginas a través de la función de devolución de llamada.
7.  Rellene una estructura [**PROPSHEETHEADER**](/windows/win32/api/prsht/ns-prsht-propsheetheadera_v2) para mostrar la hoja de propiedades. El miembro **phpage** recibe un puntero a una matriz de identificadores de página recopilados por la función de devolución de llamada. El miembro **nPages** recibe el número de páginas de la matriz de identificadores de página.
8.  Para mostrar la hoja de propiedades, llame a la función [**hoja**](/windows/win32/api/prsht/nf-prsht-propertysheeta) .

Si se cambian los datos de cualquier página y se hace clic en los botones **Aceptar** o **aplicar** , la ventana identificada por el miembro **hwndParentSheet** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) recibirá un mensaje de [**notificación de \_ \_ \_ cambio de WM ADSPROP**](wm-adsprop-notify-change.md) . Este mensaje es estrictamente una notificación y no requiere ninguna acción específica.

Cuando se cierra la página, la ventana identificada por el miembro **hwndHidden** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) recibirá un mensaje de notificación de [**\_ \_ \_ cierre \_ de hoja DSA de WM**](wm-dsa-sheet-close-notify.md) . Este mensaje es estrictamente una notificación y no requiere que se realice ninguna acción específica.

En algunos casos, las hojas de propiedades existentes deberán mostrar una hoja de propiedades secundaria. Por ejemplo, si muestra la hoja de propiedades de un objeto de usuario y selecciona el **miembro de** la página, se mostrará una lista de los grupos de los que el usuario es miembro. Si hace doble clic en uno de estos grupos de la lista, se mostrará la hoja de propiedades de ese grupo. La hoja de propiedades principal no muestra la hoja secundaria por sí misma. Solicita que el host muestre la hoja secundaria mediante el envío de un mensaje de [**\_ \_ \_ \_ notificación**](wm-dsa-sheet-create-notify.md) de la hoja de datos de WM DSA a la ventana identificada por el miembro **hwndHidden** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) . El *wParam* de la **hoja de WM \_ DSA \_ \_ crear \_** mensaje de notificación es un puntero a una estructura de [**\_ información de \_ página \_ de DSA sec**](dsa-sec-page-info.md) que contiene información sobre la hoja de propiedades secundaria y el objeto que representa. En respuesta a este mensaje, el host de la hoja de propiedades debe mostrar la hoja de propiedades secundaria de la misma manera que se mostró anteriormente. Después de procesar el mensaje de **\_ \_ \_ \_ notificación** de la hoja de DSA de WM, el receptor del mensaje debe liberar la estructura de  **información de página de DSA \_ \_ \_ sec** pasando el valor de wParam a la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

## <a name="duplicating-the-behavior-of-the-clsid_dspropertypages-object"></a>Duplicar el comportamiento del objeto CLSID \_ DsPropertyPages

**Para duplicar el comportamiento del \_ objeto CLSID DsPropertyPages**

1.  Enumere los valores del atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) o [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) para el especificador de presentación de la clase de objeto. Cada valor es una cadena que contiene un número, seguido de una coma, seguida de la representación de cadena del identificador de clase de la extensión de la página de propiedades. Para obtener más información sobre el formato de los valores del especificador de presentación de las páginas de propiedades, vea [registrar la página de propiedades de un objeto com en un especificador de presentación](registering-the-property-page-com-object-in-a-display-specifier.md).
2.  Convierta cada cadena de identificador de clase en un **CLSID** mediante la función [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .
3.  Ordene los identificadores de clase de extensión por el número que precede a cada cadena de identificador de clase en el valor de atributo. Si dos números son idénticos, ordene los identificadores de clase en el orden en que se obtienen los valores de atributo del servidor de Active Directory.
4.  Enumera los identificadores de clase de extensión y crea una instancia de cada extensión.
5.  Para cada extensión, en el orden anterior, llame a [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) de la extensión con la misma información que se describe en el paso 4 del procedimiento de la hoja de propiedades Hosting a Active Directory Users and Computers.
6.  Para cada extensión, en el orden indicado anteriormente, llame a [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) de la extensión con la misma información que se describe en el paso 5 del procedimiento de la hoja de propiedades hospedar un Active Directory usuarios y equipos.

Si es posible, use el objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) para crear las páginas en lugar de hacerlo manualmente. El **\_ DsPropertyPages CLSID** se ha optimizado y controla correctamente los casos de error, como cuando no hay ningún especificador de pantalla disponible para la configuración regional actual. Además, el **objeto \_ DsPropertyPages CLSID** puede cambiar en el futuro, lo que significa que las hojas de propiedades pueden no coincidir exactamente con las mostradas por el complemento MMC usuarios y equipos de Active Directory.

## <a name="special-programming-elements"></a>Elementos de programación especiales

Actualmente, los siguientes elementos de programación no se definen en un archivo de encabezado publicado. Para usar estos elementos, debe definirlos usted mismo en el formato exacto que se muestra en la página de referencia determinada.

-   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
-   [**PROPSHEETCFG**](propsheetcfg.md)
-   [**\_notificación de \_ cierre de hoja DSA \_ de WM \_**](wm-dsa-sheet-close-notify.md)
-   [**\_ \_ \_ crear notificación de la hoja DSA de WM \_**](wm-dsa-sheet-create-notify.md)
-   [**información de página de DSA \_ s \_ \_**](dsa-sec-page-info.md)

## <a name="example-code"></a>Código de ejemplo

En el ejemplo de código de C++ siguiente se muestra una manera segura de definir estos elementos que seguirán funcionando aunque estos elementos se hayan definido en un archivo de encabezado publicado en el futuro.


```C++
#ifndef CFSTR_DS_PROPSHEETCONFIG
    #define CFSTR_DS_PROPSHEETCONFIG_W L"DsPropSheetCfgClipFormat"
    #define CFSTR_DS_PROPSHEETCONFIG_A "DsPropSheetCfgClipFormat"

    #ifdef UNICODE
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_W
    #else
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_A
    #endif //UNICODE
#endif //CFSTR_DS_PROPSHEETCONFIG


#ifndef WM_ADSPROP_SHEET_CREATE
    #define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
#endif


#ifndef WM_DSA_SHEET_CREATE_NOTIFY
    #define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
#endif


#ifndef WM_DSA_SHEET_CLOSE_NOTIFY
    #define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5) 
#endif


#ifndef DSA_SEC_PAGE_INFO
    typedef struct _DSA_SEC_PAGE_INFO
    {
        HWND    hwndParentSheet;
        DWORD   offsetTitle;
        DSOBJECTNAMES dsObjectNames;
    } DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
#endif //DSA_SEC_PAGE_INFO

#ifndef PROPSHEETCFG
    typedef struct _PROPSHEETCFG
    {  
        LONG_PTR lNotifyHandle;  
        HWND hwndParentSheet;  
        HWND hwndHidden;  
        WPARAM wParamSheetClose;
    } PROPSHEETCFG, *PPROPSHEETCFG;
#endif //PROPSHEETCFG
```



 

