---
title: Usar el objeto de Active Desktop
description: Este artículo contiene información sobre el objeto ActiveDesktop que forma parte de la API de Shell de Windows. Este objeto, a través de su interfaz IActiveDesktop, permite agregar, quitar y cambiar elementos en el escritorio.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Objeto ActiveDesktop
- Active Desktop
- enumeración, elementos de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487566"
---
# <a name="using-the-active-desktop-object"></a>Usar el objeto de Active Desktop

\[Esta característica solo se admite en Windows XP o versiones anteriores. \]

Este artículo contiene información sobre el objeto **ActiveDesktop** que forma parte de la API de Shell de Windows. Este objeto, a través de su interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , permite agregar, quitar y cambiar elementos en el escritorio.

## <a name="overview-of-the-active-desktop-interface"></a>Información general de la interfaz de Active Desktop

-   [Acceso a Active Desktop](#accessing-the-active-desktop)
-   [Agregar un elemento de escritorio](#adding-a-desktop-item)
-   [Enumerar los elementos del escritorio](#enumerating-the-desktop-items)

Active Desktop es una característica incluida en Microsoft Internet Explorer 4,0 que permite incluir documentos y elementos HTML (como los controles ActiveX de Microsoft y applets de Java) directamente en el escritorio. La interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , que forma parte de la API de Shell de Windows, se usa para agregar, quitar y modificar elementos en el escritorio mediante programación. Los elementos de Active Desktop también se pueden agregar mediante un archivo de formato de definición de canal (CDF).

### <a name="accessing-the-active-desktop"></a>Acceso a Active Desktop

Para obtener acceso a Active Desktop, una aplicación cliente necesitaría crear una instancia del objeto ActiveDesktop (CLSID \_ ActiveDesktop) con la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y recuperar un puntero a la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) del objeto.

En el ejemplo siguiente se muestra cómo recuperar un puntero a la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>Agregar un elemento de escritorio

Hay tres métodos que puede usar para agregar un elemento de escritorio: [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)y [**IActiveDesktop:: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Cada elemento de escritorio agregado a Active Desktop debe tener una dirección URL de origen diferente.

Los métodos [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) y [**IActiveDesktop:: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) proporcionan la opción para mostrar las diversas interfaces de usuario que se pueden mostrar antes de agregar un elemento de escritorio al escritorio activo. Las interfaces de comprueban si los usuarios desean agregar el elemento de escritorio a su escritorio activo. Las interfaces también notifican a los usuarios los riesgos de seguridad que están garantizados por la configuración de la zona de seguridad de la dirección URL y solicitan a los usuarios si desean crear una suscripción para este elemento de escritorio. Ambos métodos también proporcionan una manera de suprimir las interfaces de usuario. El método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) requiere una llamada a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) para actualizar el registro. En el caso de **IActiveDesktop:: AddDesktopItemWithUI**, la aplicación cliente debe liberar inmediatamente la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) y, a continuación, utilizar la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar una interfaz en una instancia del objeto **ActiveDesktop** que incluye el elemento de escritorio recién agregado.

El método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) agrega el elemento de escritorio especificado al escritorio activo sin ninguna interfaz de usuario, a menos que la configuración de la zona de seguridad de la dirección URL lo impida. Si la configuración de la zona de seguridad de la dirección URL no permite agregar el elemento de escritorio sin preguntar al usuario, se produce un error en el método. **IActiveDesktop:: AddDesktopItem** también requiere una llamada a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) para actualizar el registro.

En el ejemplo siguiente se muestra cómo agregar un elemento de escritorio con el método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>Enumerar los elementos del escritorio

Para enumerar los elementos de escritorio instalados actualmente en el escritorio activo, la aplicación cliente debe recuperar el número total de elementos de escritorio instalados mediante el método [**IActiveDesktop:: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) y, a continuación, crear un bucle que recupere la estructura del [**componente**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) para cada elemento de escritorio mediante una llamada al método [**IActiveDesktop:: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) mediante el uso del índice de elemento de escritorio.

En el ejemplo siguiente se muestra una manera de enumerar los elementos del escritorio.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 