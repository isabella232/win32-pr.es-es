---
description: En la sección obtener el identificador de una carpeta se describen dos métodos para obtener el puntero de un objeto de espacio de nombres a una lista de identificadores de elementos (PIDL).
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: Obtener información sobre el contenido de una carpeta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997209"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>Obtener información sobre el contenido de una carpeta

En la sección [obtener el identificador de una carpeta](folder-id.md) se describen dos métodos para obtener el puntero de un objeto de espacio de nombres a una lista de identificadores de elementos (PIDL). Una pregunta obvia es: una vez que tenga un PIDL, ¿qué puede hacer con él? Una pregunta relacionada es: ¿Qué ocurre si no funciona o es adecuado para su aplicación? La respuesta a ambas preguntas requiere tener una visión más detallada de cómo se implementa el espacio de nombres. La clave es la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

-   [Uso de la interfaz IShellFolder](#using-the-ishellfolder-interface)
-   [Enumerar el contenido de una carpeta](#enumerating-the-contents-of-a-folder)
-   [Determinar los nombres para mostrar y otras propiedades](#determining-display-names-and-other-properties)
-   [Obtener un puntero a la interfaz IShellFolder de una subcarpeta](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [Determinar la carpeta primaria de un objeto](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>Uso de la interfaz IShellFolder

Anteriormente en esta documentación, las carpetas de espacio de nombres se denominaban objetos. Aunque, en ese momento, el término se usó en un sentido flexible, en realidad también es cierto en un sentido estricto. Cada carpeta de espacio de nombres se representa mediante un objeto de modelo de objetos componentes (COM). Cada objeto de carpeta expone una serie de interfaces que se pueden usar para una amplia variedad de tareas. Es posible que algunas interfaces que son opcionales no se expongan en todas las carpetas. Sin embargo, todas las carpetas deben exponer la interfaz fundamental, [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).

El primer paso en el uso de un objeto de carpeta es recuperar un puntero a su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Además de proporcionar acceso a las otras interfaces del objeto, **IShellFolder** expone un grupo de métodos que controlan varias tareas comunes, algunas de las cuales se describen en esta sección.

Para recuperar un puntero a la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de un objeto de espacio de nombres, primero debe llamar a [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder). Esta función devuelve un puntero a la interfaz **IShellFolder** de la raíz del espacio de nombres, el escritorio. Una vez que tenga la interfaz **IShellFolder** del escritorio, hay varias formas de continuar.

Si ya tiene el PIDL de la carpeta que le interesa, por ejemplo, mediante una llamada a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), puede recuperar su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) llamando al método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) del escritorio. Si tiene la ruta de acceso de un objeto del sistema de archivos, primero debe obtener su PIDL llamando al método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) de escritorio y, a continuación, llamar a **IShellFolder:: BindToObject**. Si ninguno de estos métodos es aplicable, puede usar otros métodos **IShellFolder** para navegar por el espacio de nombres. Para obtener más información, vea [navegar por el espacio de nombres](navigate.md).

## <a name="enumerating-the-contents-of-a-folder"></a>Enumerar el contenido de una carpeta

Lo primero que normalmente desea hacer con una carpeta es averiguar lo que contiene. Primero debe llamar al método [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) de la carpeta. La carpeta creará un objeto de enumeración OLE estándar y devolverá su interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) . Esta interfaz expone cuatro métodos estándar ([**clonar**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone), [**siguiente**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next), [**restablecer**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)y [**omitir**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)) que se pueden usar para enumerar el contenido de la carpeta.

El procedimiento básico para enumerar el contenido de una carpeta es:

1.  Llame al método Folders [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) para recuperar un puntero a la interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de un objeto de enumeración.
2.  Pase un PIDL sin asignar a [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). A **continuación** se encarga de asignar el PIDL, pero la aplicación debe desasignarlo cuando ya no se necesite. Cuando **siguiente** devuelve, el PIDL contendrá solo el identificador de elemento del objeto y los caracteres **nulos** de terminación. En otras palabras, se trata de una PIDL de un solo nivel, relativa a la carpeta, no a un PIDL completo.
3.  Repita el paso 2 hasta que [**siguiente**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) devuelva S \_ false para indicar que se han enumerado todos los elementos.
4.  Llame a **IEnumIDList:: Release** para liberar el objeto de enumeración.

> [!Note]  
> Es importante realizar un seguimiento de si está trabajando con una PIDL completa o relativa. Algunas funciones y métodos aceptarán, pero otros solo adoptarán uno u otro.

 

Los tres métodos restantes de [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) ([**restablecer**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset), [**omitir**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)y [**clonar**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) son útiles si necesita realizar enumeraciones repetidas de la carpeta. Permiten restablecer la enumeración, omitir uno o más objetos y hacer una copia del objeto de enumeración para conservar su estado.

## <a name="determining-display-names-and-other-properties"></a>Determinar los nombres para mostrar y otras propiedades

Una vez que ha enumerado todos los PIDL de elementos contenidos en una carpeta, puede averiguar qué tipo de objetos representan. La interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) proporciona una serie de métodos útiles, dos de los cuales se describen aquí. Más adelante se explican otros métodos **IShellFolder** y otras interfaces de carpeta de Shell.

Una de las propiedades más útiles es el nombre para mostrar del objeto. Para recuperar el nombre para mostrar de un objeto, pase su PIDL a [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Aunque el objeto puede encontrarse en cualquier lugar debajo de la carpeta principal del espacio de nombres, su PIDL debe ser relativa a la carpeta.

[**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) devuelve el nombre para mostrar como parte de una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Dado que extraer el nombre para mostrar de una estructura **Strret** puede ser un poco complicado, el Shell proporciona dos funciones que realizan el trabajo por usted, [**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) y [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa). Ambas funciones toman una estructura **Strret** y devuelven el nombre para mostrar como una cadena normal. Solo difieren en cómo se asigna la cadena.

Además de su nombre para mostrar, un objeto puede tener varios atributos, como, por ejemplo, si se trata de una carpeta o si puede moverse. Puede recuperar los atributos de un objeto pasando su PIDL a [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof). La lista completa de atributos es bastante grande, por lo que debería ver la referencia para obtener más información. Tenga en cuenta que el PIDL que pasa a **GetAttributesOf** debe ser de un solo nivel. En concreto, **IShellFolder:: GetAttributesOf** aceptará el PIDL devuelto por [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). Puede pasar una matriz de PIDL y **GetAttributesOf** devolverá los atributos que todos los objetos de la matriz tengan en común.

Si tiene la ruta de acceso completa o el PIDL de un objeto, [**SHGetFileInfo**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) proporciona una manera sencilla de recuperar información sobre un objeto que es suficiente para muchos propósitos. **SHGetFileInfo** toma una ruta de acceso completa o PIDL y devuelve una gran variedad de información sobre el objeto, incluidos:

-   Nombre para mostrar del objeto
-   Atributos del objeto
-   Identificadores de los iconos del objeto
-   Identificador de la lista de imágenes del sistema
-   La ruta de acceso del archivo que contiene el icono del objeto.

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>Obtener un puntero a la interfaz IShellFolder de una subcarpeta

Puede determinar si la carpeta contiene todas las subcarpetas llamando a [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) y comprobando si la marca de \_ carpeta SFGAO está establecida. Si un objeto es una carpeta, puede enlazar a él, lo que le proporciona un puntero a su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Para enlazar a una subcarpeta, llame al método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) de la carpeta principal. Este método toma el PIDL de la subcarpeta y devuelve un puntero a su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Una vez que tenga este puntero, puede usar los métodos **IShellFolder** para enumerar el contenido de las subcarpetas, determinar sus propiedades, etc.

## <a name="determining-an-objects-parent-folder"></a>Determinar la carpeta primaria de un objeto

Si tiene PIDL de un objeto, es posible que necesite un identificador a una de las interfaces expuestas por su carpeta principal. Por ejemplo, si desea determinar el nombre para mostrar asociado a un PIDL mediante [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), primero debe recuperar la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del elemento primario del objeto. Es posible hacerlo con las técnicas descritas en las secciones anteriores. Sin embargo, un enfoque mucho más sencillo es usar la función de Shell [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent). Esta función toma el PIDL completo de un objeto y devuelve un puntero de interfaz especificado en la carpeta principal. Opcionalmente, también devuelve el PIDL de nivel único del elemento para su uso en métodos como [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).

La siguiente aplicación de consola de ejemplo recupera el PIDL de la carpeta especial del sistema y devuelve su nombre para mostrar.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



En primer lugar, la aplicación usa [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) para recuperar el PIDL de la carpeta del sistema. A continuación, llama a [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent), que devuelve un puntero a la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de la carpeta primaria y la PIDL de la carpeta del sistema en relación con su elemento primario. A continuación, usa el método [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) de la carpeta principal para recuperar el nombre para mostrar de la carpeta del sistema. Dado que **GetDisplayNameOf** devuelve una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) se usa para convertir el nombre para mostrar en una cadena normal. Después de mostrar el nombre para mostrar, se liberan los punteros de interfaz y se libera PIDL del sistema. Tenga en cuenta que no debe liberar el PIDL relativo devuelto por **SHBindToParent**.

 

 
