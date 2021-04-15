---
description: El procedimiento para implementar una extensión de espacio de nombres es similar al de cualquier otro objeto de modelo de objetos componentes (COM) en proceso.
title: Implementar las interfaces de objeto de carpeta básicas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985662"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>Implementar las interfaces de objeto de carpeta básicas

El procedimiento para implementar una extensión de espacio de nombres es similar al de cualquier otro objeto de modelo de objetos componentes (COM) en proceso. Todas las extensiones deben admitir tres interfaces principales que proporcionan al explorador de Windows la información básica necesaria para mostrar las carpetas de la extensión en la vista de árbol. Sin embargo, para hacer un uso completo de las capacidades del explorador de Windows, la extensión también debe exponer una o varias interfaces opcionales que admitan características más sofisticadas, como menús contextuales o arrastrar y colocar, y proporcionar una vista de carpeta.

En este documento se explica cómo implementar las interfaces principales y opcionales que el explorador de Windows llama para obtener información sobre el contenido de la extensión. Para obtener información sobre cómo implementar una vista de carpetas y cómo personalizar el explorador de Windows, consulte [implementar una vista de carpeta](../lwef/nse-folderview.md).

-   [Implementación y registro básicos](#basic-implementation-and-registration)
    -   [Registrar una extensión](#registering-an-extension)
-   [Controlar PIDL](#handling-pidls)
    -   [Crear una estructura SHITEMID](#creating-an-shitemid-structure)
    -   [Construir un PIDL](#constructing-a-pidl)
    -   [Interpretar PIDL](#interpreting-pidls)
-   [Implementar las interfaces principales](#implementing-the-primary-interfaces)
    -   [Interfaz IPersistFolder](#ipersistfolder-interface)
    -   [Interfaz IShellFolder](#ishellfolder-interface)
    -   [Interfaz IEnumIDList](#ienumidlist-interface)
-   [Implementar las interfaces opcionales](#implementing-the-optional-interfaces)
    -   [IExtractIcon](#iextracticon)
    -   [IContextMenu](#icontextmenu)
    -   [IQueryInfo](#iqueryinfo)
    -   [IDataObject e IDropTarget](#idataobject-and-idroptarget)
-   [Trabajar con la implementación de vista de carpeta de Shell predeterminada](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>Implementación y registro básicos

Como servidor COM en proceso, el archivo DLL debe exponer varias funciones y interfaces estándar:

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Estas funciones e interfaces se implementan de la misma manera que para la mayoría de los demás objetos COM. Para obtener más información, consulte la [documentación de com](../com/the-component-object-model.md).

### <a name="registering-an-extension"></a>Registrar una extensión

Al igual que con todos los objetos COM, debe crear un GUID de identificador de clase (CLSID) para la extensión. Registre el objeto creando una subclave de **\_ clase HKEY \_ raíz** \\ **CLSID** denominada para el CLSID de la extensión. El archivo DLL se debe registrar como un servidor en proceso y debe especificar el modelo de subprocesos de apartamento. Puede personalizar el comportamiento de la carpeta raíz de una extensión agregando una variedad de subclaves y valores a la clave CLSID de la extensión.

Algunos de estos valores solo se aplican a las extensiones con puntos de Unión virtuales. Estos valores no se aplican a las extensiones cuyos puntos de Unión son carpetas del sistema de archivos. Para obtener más información, vea [especificar la ubicación de una extensión de espacio de nombres](nse-junction.md). Para modificar el comportamiento de una extensión con un punto de Unión virtual, agregue uno o varios de los siguientes valores a la clave CLSID de la extensión:

-   WantsFORPARSING. Normalmente, el nombre de análisis de una extensión con un punto de Unión virtual tendrá el formato:: {*GUID*}. Normalmente, las extensiones de este tipo contienen elementos virtuales. Sin embargo, algunas extensiones, como mis documentos, se corresponden realmente con las carpetas del sistema de archivos, aunque tengan puntos de Unión virtuales. Si la extensión representa objetos del sistema de archivos de esta manera, puede establecer el valor de WantsFORPARSING. Después, el explorador de Windows solicitará el nombre de análisis de la carpeta raíz llamando al método [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) del objeto de la carpeta con *UFlags* establecido en **SHGDN \_ FORPARSING** y *PIDL* establecido en un único puntero vacío a una lista de identificadores de elementos (PIDL). Un PIDL vacío solo contiene un terminador. Después, el método debe devolver el nombre de análisis de la carpeta raíz:: {*GUID*}.
-   HideFolderVerbs. Los verbos registrados en la **carpeta \_ \_ raíz de las clases HKEY** \\  suelen estar asociados a todas las extensiones. Aparecen en el menú contextual de la extensión y se pueden invocar mediante [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea). Para evitar que cualquiera de estos verbos se asocie a la extensión, establezca el valor de HideFolderVerbs.
-   HideAsDelete. Si un usuario intenta eliminar la extensión, el explorador de Windows ocultará en su lugar la extensión.
-   HideAsDeletePerUser. Este valor tiene el mismo efecto que HideAsDelete, pero por usuario. La extensión solo está oculta para los usuarios que han intentado eliminarla. La extensión es visible para todos los demás usuarios.
-   QueryForOverlay. Establezca este valor para indicar que el icono de la carpeta raíz puede tener una superposición de iconos. El objeto de carpeta debe admitir la interfaz [**IShellIconOverlay**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) . Antes de que el explorador de Windows muestre el icono de la carpeta raíz, se solicitará un icono de superposición llamando a uno de los dos métodos **IShellIconOverlay** con *pidlItem* establecido en un PIDL vacío.

Los valores y subclaves restantes se aplican a todas las extensiones:

-   Para especificar el nombre para mostrar de la carpeta de punto de unión de la extensión, establezca el valor predeterminado de la subclave CLSID de la extensión en una cadena adecuada.
-   Cuando el cursor se mantiene sobre una carpeta, normalmente se muestra un recuadro informativo que describe el contenido de la carpeta. Para proporcionar un recuadro informativo a la carpeta raíz de la extensión, cree un valor de **reg \_ SZ** para la clave CLSID de la extensión y establézcalo en una cadena adecuada.
-   Para especificar un icono personalizado para la carpeta raíz de la extensión, cree una subclave de la subclave CLSID de la extensión denominada **DefaultIcon**. Establezca el valor predeterminado de **DefaultIcon** en un valor de **reg \_ SZ** que contenga el nombre del archivo que contiene el icono, seguido de una coma, seguido de un signo menos, seguido del índice del icono de ese archivo.
-   De forma predeterminada, el menú contextual de la carpeta raíz de la extensión contendrá los elementos definidos en la **\_ \_ \\ carpeta raíz HKEY classes**. Si ha establecido las marcas SFGAO XXX adecuadas, se agregan los elementos **eliminar**, **cambiar nombre** y **propiedades** \_ . Puede agregar otros elementos al menú contextual de la carpeta raíz o invalidar los elementos existentes, de forma muy similar a como lo haría con un [tipo de archivo](fa-file-types.md). Cree una subclave de **Shell** en la clave CLSID de la extensión y defina los comandos como se describe en [extender menús contextuales](context.md).
-   Si necesita una manera más flexible de controlar el menú contextual de la carpeta raíz, puede implementar un [controlador de menú contextual](context-menu-handlers.md). Para registrar el controlador de menú contextual, cree una clave **ShellEx** en la clave CLSID de la extensión. Registre el CLSID del controlador como lo haría para los controladores de la [extensión de Shell de creación](handlers.md)convencionales.
-   Para agregar una página a la hoja de propiedades de la carpeta raíz, asigne a la carpeta el atributo **SFGAO \_ HASPROPSHEET** e implemente un controlador de la [hoja de propiedades](propsheet-handlers.md). Para registrar el controlador de la hoja de propiedades, cree una clave **ShellEx** en la clave CLSID de la extensión. Registre el CLSID del controlador como lo haría para los controladores de la [extensión de Shell de creación](handlers.md)convencionales.
-   Para especificar los atributos de la carpeta raíz, agregue una subclave **ShellFolder** a la subclave CLSID de la extensión. Cree un valor de atributos y establézcalo en la combinación adecuada de marcas [**SFGAO \_ XXX**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) .

En la tabla siguiente se enumeran algunos atributos usados comúnmente para las carpetas raíz.



| Marca                | Value      | Descripción                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_carpeta SFGAO       | 0x20000000 | La carpeta raíz de la extensión contiene uno o varios elementos.                                                                                                                                                                                                                                                           |
| SFGAO \_ HASSUBFOLDER | 0x80000000 | La carpeta raíz de la extensión contiene una o varias subcarpetas. El explorador de Windows colocará un signo más (+) junto al icono de carpeta.                                                                                                                                                                               |
| SFGAO \_ CANDELETE    | 0x00000020 | El usuario puede eliminar la carpeta raíz de la extensión. El menú contextual de la carpeta tendrá un elemento **eliminar** . Esta marca se debe establecer para los puntos de Unión que se colocan en una de las [carpetas virtuales](nse-junction.md).                                                                                 |
| SFGAO \_ CANRENAME    | 0x00000010 | El usuario puede cambiar el nombre de la carpeta raíz de la extensión. El menú contextual de la carpeta tendrá un elemento **cambiar nombre** .                                                                                                                                                                                                   |
| SFGAO \_ HASPROPSHEET | 0x00000040 | La carpeta raíz de la extensión tiene una hoja de propiedades de **propiedades** . El menú contextual de la carpeta tendrá un elemento **propiedades** . Para proporcionar la hoja de propiedades, debe implementar un [controlador](propsheet-handlers.md)de la hoja de propiedades. Registre el controlador bajo la clave CLSID de la extensión, como se explicó anteriormente. |



 

En el ejemplo siguiente se muestra la entrada del registro CLSID para una extensión con el nombre para mostrar de la extensión. La extensión tiene un icono personalizado que se encuentra en el archivo DLL de la extensión con un índice de 1. Se establecen los atributos **SFGAO \_**, **SFGAO \_ HASSUBFOLDER** y **SFGAO \_ CANDELETE** .

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         (Default) = MyExtension
         InfoTip = Some appropriate text
      DefaultIcon
         (Default) = c:\MyDir\MyExtension.dll,-1
      InProcServer32
         (Default) = c:\MyDir\MyExtension.dll
         ThreadingModel = Apartment
      ShellFolder
         Attributes = 0xA00000020
```

## <a name="handling-pidls"></a>Controlar PIDL

Todos los elementos del espacio de nombres del shell deben tener un PIDL único. El explorador de Windows asigna un PIDL a la carpeta raíz y pasa el valor a la extensión durante la inicialización. A continuación, la extensión es responsable de asignar un PIDL construido correctamente a cada uno de sus objetos y de proporcionar esos PIDL al explorador de Windows a petición. Cuando el shell usa un PIDL para identificar uno de los objetos de la extensión, la extensión debe ser capaz de interpretar el PIDL e identificar el objeto determinado. La extensión también debe asignar un [**nombre para mostrar**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) y un *nombre de análisis* a cada objeto. Dado que la PIDL se usa prácticamente en cada interfaz de carpeta, las extensiones suelen implementar un único *Administrador de PIDL* para controlar todas estas tareas.

El término PIDL es corto para una estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o un puntero a una estructura de este tipo, dependiendo del contexto. Como se declara, una estructura **ITEMIDLIST** tiene un solo miembro, una estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . La estructura **ITEMIDLIST** de un objeto es realmente una matriz empaquetada de dos o más estructuras **SHITEMID** . El orden de estas estructuras define una ruta de acceso a través del espacio de nombres, de la misma manera que c: myPath \\ \\ myPath define una ruta de acceso a través del sistema de archivos. Normalmente, el PIDL de un objeto constará de una serie de estructuras **SHITEMID** que se corresponden con las carpetas que definen la ruta de acceso del espacio de nombres, seguida de la estructura **SHITEMID** del objeto, seguida de un terminador.

El terminador es una estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , con el miembro *CB* establecido en **null**. El terminador es necesario porque el número de estructuras **SHITEMID** de PIDL de un objeto depende de la ubicación del objeto en el espacio de nombres del shell y del punto inicial de la ruta de acceso. Además, el tamaño de las distintas estructuras **SHITEMID** puede variar. Cuando recibe un PIDL, no tiene una forma sencilla de determinar su tamaño o incluso el número total de estructuras de **SHITEMID** . En su lugar, debe "recorrer" la matriz empaquetada, estructurada por estructura, hasta alcanzar el terminador.

Para crear un PIDL, la aplicación debe:

1.  Cree una estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para cada uno de sus objetos.
2.  Ensamble las estructuras [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) relevantes en un PIDL.

### <a name="creating-an-shitemid-structure"></a>Crear una estructura SHITEMID

La estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de un objeto identifica de forma única el objeto dentro de su carpeta. De hecho, un tipo de PIDL utilizado por muchos de los métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) solo se compone de la estructura **SHITEMID** del objeto, seguida de un terminador. La definición de una estructura **SHITEMID** es:


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



El miembro *atenerse* es el identificador del objeto. Dado que la longitud de la extensión *no está definida* y puede variar, el miembro *CB* se establece en el tamaño de la estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , en bytes.

Dado que *no se normaliza* ni la longitud ni el contenido de la extensión, puede usar cualquier esquema que desee *asignar a los objetos* . El único requisito es que no se pueden tener dos objetos en la misma carpeta con valores idénticos. Sin embargo, por motivos de rendimiento, la estructura de [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) debe alinearse con **DWORD**. En otras palabras, debe construir los valores de *respetar* tal que *CB* sea un múltiplo entero de 4.

Normalmente, se *hace referencia a* una estructura definida por la extensión. Además del identificador del objeto, esta estructura se usa a menudo para contener una gran variedad de información relacionada, como el tipo o los atributos del objeto. Los objetos de carpeta de la extensión pueden extraer rápidamente la información de PIDL en lugar de tener que consultarla.

> [!Note]  
> Uno de los aspectos más importantes del diseño de una estructura de datos para un PIDL es hacer que la estructura sea persistente y se pueda transportar. En el contexto de PIDL, el significado de estos términos es:
>
> -   Con persistencia. Con frecuencia, el sistema coloca PIDL en varios tipos de almacenamiento a largo plazo, como archivos de acceso directo. Después, puede recuperar estos PIDL desde el almacenamiento más adelante, probablemente después de reiniciar el sistema. Un PIDL que se ha recuperado del almacenamiento debe seguir siendo válido y significativo para la extensión. Este requisito significa, por ejemplo, que no se deben usar punteros o manipuladores en la estructura PIDL. Los PIDL que contienen este tipo de datos normalmente no tendrán sentido cuando el sistema los recupere posteriormente del almacenamiento.
> -   Transportables. Un PIDL debe seguir siendo significativo cuando se transporta de un equipo a otro. Por ejemplo, un PIDL puede escribirse en un archivo de acceso directo, copiarse en un disquete y transportarse a otro equipo. Ese PIDL debe seguir siendo significativo para la extensión que se ejecuta en el segundo equipo. Por ejemplo, para asegurarse de que los PIDL sean transportables, use explícitamente caracteres ANSI o Unicode. Evite tipos de datos como **TCHAR** o **LPTSTR**. Si usa esos tipos de datos, un PIDL creado en un equipo que ejecute una versión Unicode de la extensión no se podrá leer con una versión ANSI de esa extensión que se ejecute en un equipo diferente.

 

En la declaración siguiente se muestra un ejemplo simple de una estructura de datos.


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



El miembro **CB** se establece en el tamaño de la estructura **MYPIDLDATA** . Este miembro convierte **MYPIDLDATA** en una estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) válida, en y de sí misma. El resto de los miembros son equivalentes a **los miembros** de una estructura **SHITEMID** y contienen datos privados. El miembro **dwType** es un valor definido por la extensión que indica el tipo de objeto. En este ejemplo, **dwType** se establece en **true** para las carpetas y **false** en caso contrario. Este miembro le permite, por ejemplo, determinar rápidamente si el objeto es o no una carpeta. El miembro **wszDisplayName** contiene el nombre para mostrar del objeto. Dado que no asignaría el mismo nombre para mostrar a dos objetos diferentes en la misma carpeta, el nombre para mostrar también sirve como identificador de objeto. En este ejemplo, **wszDisplayName** se establece en 40 caracteres para garantizar que la estructura **SHITEMID** se alineará con **DWORD**. Para limitar el tamaño de PIDL, puede usar una matriz de caracteres de longitud variable y ajustar el valor de CB en consecuencia. Rellene la cadena de presentación con suficientes \\ caracteres ' 0 ' para mantener la alineación **DWORD** de la estructura. Otros miembros que pueden ser útiles para colocar en la estructura incluyen el tamaño del objeto, los atributos o el nombre de análisis.

### <a name="constructing-a-pidl"></a>Construir un PIDL

Una vez que haya definido las estructuras [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para los objetos, puede usarlas para construir un PIDL. PIDL se puede construir para una variedad de propósitos, pero en la mayoría de las tareas se usa uno de los dos tipos de PIDL. La más simple, una PIDL de un solo nivel, identifica el objeto relativo a su carpeta principal. Muchos de los métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) utilizan este tipo de PIDL. Un PIDL de nivel único contiene la estructura **SHITEMID** del objeto, seguida de un terminador. Un PIDL completo define una ruta de acceso a través de la jerarquía de espacios de nombres desde el escritorio hasta el objeto. Este tipo de PIDL se inicia en el escritorio y contiene una estructura **SHITEMID** para cada carpeta de la ruta de acceso, seguida del objeto y el terminador. Un PIDL completo identifica de forma única el objeto en todo el espacio de nombres del shell.

La manera más sencilla de construir un PIDL es trabajar directamente con la propia estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Cree una estructura **ITEMIDLIST** , pero asigne suficiente memoria para contener todas las estructuras [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . La dirección de esta estructura apuntará a la estructura **SHITEMID** inicial. Defina valores para los miembros de esta estructura inicial y, a continuación, anexe tantas estructuras **SHITEMID** adicionales como necesite, en el orden adecuado. En el procedimiento siguiente se describe cómo crear un PIDL de nivel único. Contiene dos estructuras **SHITEMID** : una estructura **MYPIDLDATA** seguida de un terminador:

1.  Use la función [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar memoria para el PIDL. Asigne suficiente memoria para los datos privados más un **USHORT** (dos bytes) para el terminador. Convierta el resultado en LPMYPIDLDATA.
2.  Establezca el miembro CB de la primera estructura **MYPIDLDATA** en el tamaño de esa estructura. En este ejemplo, se debería establecer **CB** en SIZEOF (MYPIDLDATA). Si desea usar una estructura de longitud variable, tendrá que calcular el valor de **CB**.
3.  Asigne los valores adecuados a los miembros de datos privados.
4.  Calcula la dirección de la siguiente estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . Convierta la dirección de la estructura MYPIDLDATA actual a LPBYTE y agregue ese valor al valor de **CB** determinado en el paso 3.
5.  En este caso, la siguiente estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) es el terminador. Establezca el miembro **CB** de la estructura en cero.

Para PIDL más largos, asigne suficiente memoria y repita los pasos 3-5 para cada estructura de [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) adicional.

La función de ejemplo siguiente toma el tipo y el nombre para mostrar de un objeto y devuelve el PIDL de un solo nivel del objeto. La función supone que el nombre para mostrar, incluido el carácter **nulo** de terminación, no supera el número de caracteres declarado para la estructura **MYPIDLDATA** . Si esa hipótesis deja de ser errónea, la función [**StringCbCopyW**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) truncará el nombre para mostrar. La variable **g \_ pMalloc** es un puntero [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) creado en otro lugar y almacenado en una variable global.


```C++
LPITEMIDLIST CreatePIDL(DWORD dwType, LPCWSTR pwszDisplayName)
{
    LPMYPIDLDATA   pidlOut;
    USHORT         uSize;

    pidlOut = NULL;

    //Calculate the size of the MYPIDLDATA structure.
    uSize = sizeof(MYPIDLDATA);

    // Allocate enough memory for the PIDL to hold a MYPIDLDATA structure 
    // plus the terminator
    pidlOut = (LPMYPIDLDATA)m_pMalloc->Alloc(uSize + sizeof(USHORT));

    if(pidlOut)
    {
       //Assign values to the members of the MYPIDLDATA structure
       //that is the PIDL's first SHITEMID structure
       pidlOut->cb = uSize;
       pidlOut->dwType = dwType;
       hr = StringCbCopyW(pidlOut->wszDisplayName, 
                          sizeof(pidlOut->wszDisplayName), pwszDisplayName);
       
       // TODO: Add error handling here to verify the HRESULT returned 
       // by StringCbCopyW.

       //Advance the pointer to the start of the next SHITEMID structure.
       pidlOut = (LPMYPIDLDATA)((LPBYTE)pidlOut + pidlOut->cb);

       //Create the terminating null character by setting cb to 0.
       pidlOut->cb = 0;
    }

    return pidlOut;
```



Un PIDL completo debe tener estructuras [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para cada objeto del escritorio al objeto. La extensión recibe un PIDL completo para la carpeta raíz cuando el shell llama a [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize). Para construir un PIDL completo para un objeto, tome el PIDL que el shell haya asignado a la carpeta raíz y Anexe las estructuras **SHITEMID** que se necesitan para llevarle de la carpeta raíz al objeto.

### <a name="interpreting-pidls"></a>Interpretar PIDL

Cuando el shell o una aplicación llama a una de las interfaces de la extensión para solicitar información sobre un objeto, normalmente identificará el objeto por un PIDL. Algunos métodos, como [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), usan PIDL que son relativos a la carpeta principal y son fáciles de interpretar. Sin embargo, la extensión probablemente también recibirá PIDL completo. Después, el administrador de PIDL debe determinar a qué objetos hace referencia PIDL.

Lo que complica la tarea de asociar un objeto con un PIDL completo es que una o varias de las estructuras [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) iniciales de la PIDL pueden pertenecer a objetos que se encuentran fuera de la extensión en el espacio de nombres del shell. No se puede interpretar el significado del miembro *acatar* de esas estructuras. Lo que debe hacer la extensión es "recorrer" la lista de estructuras **SHITEMID** , hasta que llegue a la estructura que corresponde a la carpeta raíz. A partir de entonces, sabrá cómo interpretar la información de las estructuras **SHITEMID** .

Para recorrer el PIDL, tome el primer valor *CB* y agréguelo a la dirección del PIDL para avanzar el puntero hasta el inicio de la siguiente estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . A continuación, señalará al miembro *CB* de esa estructura, que puede usar para avanzar el puntero hasta el inicio de la siguiente estructura **SHITEMID** , etc. Cada vez que avance el puntero, examine la estructura **SHITEMID** para determinar si se ha alcanzado la raíz del espacio de nombres de la extensión.

## <a name="implementing-the-primary-interfaces"></a>Implementar las interfaces principales

Al igual que con todos los objetos COM, implementar una extensión es en gran medida la implementación de una colección de interfaces. En esta sección se describen las tres interfaces principales que deben implementar todas las extensiones. Se utilizan para la inicialización y para proporcionar al explorador de Windows información básica sobre el contenido de la extensión. Estas interfaces, además de una [vista de carpeta](../lwef/nse-folderview.md), son todas necesarias para una extensión funcional. Sin embargo, para aprovechar por completo las características del explorador de Windows, la mayoría de las extensiones también implementan una o varias de las interfaces opcionales.

### <a name="ipersistfolder-interface"></a>Interfaz IPersistFolder

Se llama a la interfaz [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) para inicializar un nuevo objeto Folder. El método [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) asigna un PIDL completo al nuevo objeto. Almacene este PIDL para su uso posterior. Por ejemplo, un objeto de carpeta debe usar este PIDL para construir PIDL completos para los elementos secundarios del objeto. El creador del objeto de la carpeta también puede llamar a [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) para solicitar el CLSID del objeto.

Normalmente, el método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) de la carpeta primaria crea e inicializa un objeto de carpeta. Sin embargo, cuando un usuario examina la extensión, el explorador de Windows crea e inicializa el objeto de carpeta raíz de la extensión. El PIDL que el objeto de carpeta raíz recibe a través de [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) contiene la ruta de acceso del escritorio a la carpeta raíz que necesitará para construir PIDL completo para la extensión.

### <a name="ishellfolder-interface"></a>Interfaz IShellFolder

El shell trata una extensión como una colección ordenada jerárquicamente de objetos de carpeta. La interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) es el núcleo de cualquier implementación de extensión. Representa un objeto de carpeta y proporciona al explorador de Windows una gran parte de la información necesaria para mostrar el contenido de la carpeta.

[**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) suele ser la única interfaz de carpeta distinta de [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) que expone directamente un objeto de carpeta. Aunque el explorador de Windows usa una variedad de interfaces obligatorias y opcionales para obtener información sobre el contenido de la carpeta, obtiene punteros a esas interfaces a través de **IShellFolder**.

El explorador de Windows obtiene el CLSID de la carpeta raíz de la extensión de varias maneras. Para obtener más información, vea [especificar la ubicación de una extensión de espacio de nombres](nse-junction.md) o [Mostrar una vista de Self-Contained de una extensión de espacio de nombres](nse-view.md). Después, el explorador de Windows utiliza ese CLSID para crear e inicializar una instancia de la carpeta raíz y consultar una interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . La extensión crea un objeto de carpeta para representar la carpeta raíz y devuelve la interfaz **IShellFolder** del objeto. Gran parte del resto de la interacción entre la extensión y el explorador de Windows tiene lugar a través de **IShellFolder**. El explorador de Windows llama a **IShellFolder** para:

-   Solicita un objeto que puede enumerar el contenido de la carpeta raíz.
-   Obtener varios tipos de información sobre el contenido de la carpeta raíz.
-   Solicite un objeto que exponga una de las interfaces opcionales. A continuación, se puede consultar a esas interfaces información adicional, como iconos o menús contextuales.
-   Solicite un objeto de carpeta que represente una subcarpeta de la carpeta raíz.

Cuando un usuario abre una subcarpeta de la carpeta raíz, el explorador de Windows llama a [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject). La extensión crea e inicializa un nuevo objeto Folder para representar la subcarpeta y devuelve su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Después, el explorador de Windows llama a esta interfaz para varios tipos de información, y así sucesivamente hasta que el usuario decide navegar en otro lugar del espacio de nombres del shell o cerrar el explorador de Windows.

En el resto de esta sección se describen brevemente los métodos de [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) más importantes y cómo implementarlos.

### <a name="enumobjects"></a>EnumObjects

Antes de mostrar el contenido de una carpeta en la vista de árbol, el explorador de Windows debe determinar primero lo que contiene la carpeta mediante una llamada al método [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) . Este método crea un objeto de enumeración OLE estándar que expone una interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) y devuelve el puntero de interfaz. La interfaz **IEnumIDList** permite al explorador de Windows obtener el PIDL de todos los objetos contenidos en la carpeta. Estos PIDL se usan para obtener información sobre los objetos contenidos en la carpeta. Para obtener más información, vea [IEnumIDList (interfaz](#ienumidlist-interface)).

> [!Note]  
> El método [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) solo debe devolver PIDL que sean relativos a la carpeta principal. PIDL debe contener solo la estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) del objeto, seguida de un terminador.

 

### <a name="createviewobject"></a>CreateViewObject

Antes de que se muestre el contenido de una carpeta, el explorador de Windows llama a este método para solicitar un puntero a una interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Esta interfaz la usa el explorador de Windows para administrar la vista de carpetas. Cree un objeto de vista de carpeta y devuelva su interfaz **IShellView** .

También se llama al método [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) para solicitar una de las interfaces opcionales, como [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), para la propia carpeta. La implementación de este método debe crear un objeto que exponga la interfaz solicitada y devuelva el puntero de interfaz. Si el explorador de Windows necesita una interfaz opcional para uno de los objetos contenidos en la carpeta, llamará a [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof).

### <a name="getuiobjectof"></a>GetUIObjectOf

Aunque la información básica sobre el contenido de una carpeta está disponible a través de los métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) , la extensión también puede proporcionar el explorador de Windows con varios tipos de información adicional. Por ejemplo, puede especificar iconos para el contenido de una carpeta o el menú contextual de un objeto. El explorador de Windows llama al método [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) para intentar recuperar información adicional sobre un objeto contenido en una carpeta. El explorador de Windows especifica en qué objeto desea obtener información y el IID de la interfaz correspondiente. A continuación, el objeto de carpeta crea un objeto que expone la interfaz solicitada y devuelve el puntero de interfaz.

Si la extensión permite a los usuarios transferir objetos con arrastrar y colocar o el portapapeles, el explorador de Windows llamará a [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) para solicitar una interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) o [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Para obtener más información, vea [transferir objetos de Shell con arrastrar y colocar y el portapapeles](dragdrop.md).

El explorador de Windows llama a [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) cuando desea tener el mismo tipo de información sobre la propia carpeta.

### <a name="bindtoobject"></a>BindToObject

El explorador de Windows llama al método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) cuando un usuario intenta abrir una de las subcarpetas de la extensión. Si *riid* se establece en IID \_ IShellFolder, debe crear e inicializar un objeto de carpeta que represente la subcarpeta y devolver la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del objeto.

> [!Note]  
> En la actualidad, el explorador de Windows llama a este método solo para solicitar una interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Sin embargo, no suponga que siempre será el caso. Siempre debe comprobar el valor de *riid* antes de continuar.

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

El explorador de Windows llama al método [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para convertir el PIDL de uno de los objetos de la carpeta en un nombre. Esa PIDL debe ser relativa a la carpeta principal del objeto. En otras palabras, debe contener una única estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) que no sea **null** . Dado que hay más de una posible manera de asignar nombres a los objetos, el explorador de Windows especifica el tipo de nombre estableciendo una o más marcas [**SHGDNF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf) en el parámetro *uFlags* . Se establecerá uno de los dos valores **SHGDN \_ normal** o **SHGDN \_ InFolder**, para especificar si el nombre debe ser relativo a la carpeta o relativa al escritorio. Uno de los otros tres valores, **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** o **SHGDN \_ FORPARSING**, se puede establecer para especificar para qué nombre se usará.

Debe devolver el nombre con el formato de una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Si no se establecen **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** y **SHGDN \_ FORPARSING** , se devuelve el nombre para mostrar del objeto. Si se establece la marca **SHGDN \_ FORPARSING** , el explorador de Windows solicita un nombre de análisis. Los nombres de análisis se pasan a [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) para obtener PIDL de un objeto, aunque podría encontrarse uno o varios niveles por debajo de la carpeta actual en la jerarquía de espacios de nombres. Por ejemplo, el nombre de análisis de un objeto del sistema de archivos es su ruta de acceso. Puede pasar la ruta de acceso completa de cualquier objeto del sistema de archivos al método **IShellFolder::P arsedisplayname** del escritorio, y devolverá el PIDL completo del objeto.

Aunque los nombres de análisis son cadenas de texto, no tienen por qué incluir el nombre para mostrar. Debe asignar nombres de análisis basados en lo que funcionará de manera más eficaz cuando se llama a [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) . Por ejemplo, muchas de las carpetas virtuales del shell no forman parte del sistema de archivos y no tienen una ruta de acceso completa. En su lugar, a cada carpeta se le asigna un GUID y el nombre de análisis adopta la forma:: {GUID}. Independientemente del esquema que use, debe ser capaz de "realizar un recorrido de ida y vuelta" de forma confiable. Por ejemplo, si un llamador pasa un nombre de análisis a **IShellFolder::P arsedisplayname** para recuperar PIDL de un objeto y, a continuación, pasa ese PIDL a [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) con el indicador **SHGDN \_ FORPARSING** establecido, el llamador debe recuperar el nombre de análisis original.

### <a name="getattributesof"></a>GetAttributesOf

El explorador de Windows llama al método [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) para determinar los atributos de uno o más elementos contenidos en un objeto de carpeta. El valor de *cidl* proporciona el número de elementos de la consulta y *aPidl* apunta a una lista de su PIDL.

Dado que las pruebas para algunos atributos pueden llevar mucho tiempo, el explorador de Windows normalmente restringe la consulta a un subconjunto de las marcas disponibles mediante el establecimiento de sus valores en *rfgInOut*. El método debe probar solo los atributos cuyas marcas se establecen en *rfgInOut*. Deje las marcas válidas establecidas y borre el resto. Si se incluye más de un elemento en la consulta, establezca solo las marcas que se aplican a todos los elementos.

> [!Note]  
> Los atributos deben establecerse correctamente para que un elemento se muestre correctamente. Por ejemplo, si un elemento es una carpeta que contiene subcarpetas, debe establecer la marca **\_ HASSUBFOLDER de SFGAO** . De lo contrario, el explorador de Windows no mostrará un botón + junto al icono del elemento en la vista de árbol.

 

### <a name="parsedisplayname"></a>ParseDisplayName

El método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) tiene en cierto sentido una imagen reflejada de [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). El uso más común de este método consiste en convertir el nombre de análisis de un objeto en el PIDL asociado. El nombre de análisis puede hacer referencia a cualquier objeto que se encuentra debajo de la carpeta en la jerarquía de espacios de nombres. La PIDL devuelta es relativa al objeto de carpeta que expone el método y normalmente no es completo. En otras palabras, aunque PIDL puede contener varias estructuras [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , la primera será la del propio objeto o la primera subcarpeta de la ruta de acceso de la carpeta al objeto. El autor de la llamada tendrá que anexar este PIDL al PIDL completo de la carpeta para obtener un PIDL completo para el objeto.

[**IShellFolder:**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) también se puede llamar a:P arsedisplayname para solicitar los atributos de un objeto. Dado que la determinación de todos los atributos aplicables puede llevar mucho tiempo, el autor de la llamada solo establecerá las marcas [**SFGAO \_ XXX**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) que representen información que el llamador le interese. Debe determinar cuáles de esos atributos son true para el objeto y borrar el resto de marcas.

### <a name="ienumidlist-interface"></a>Interfaz IEnumIDList

Cuando el explorador de Windows necesita enumerar los objetos contenidos en una carpeta, llama a [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects). El objeto de carpeta debe crear un objeto de enumeración que exponga la interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) y devuelva ese puntero de interfaz. El explorador de Windows normalmente usará **IEnumIDList** para enumerar el PIDL de todos los objetos contenidos en la carpeta.

[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) es una interfaz de enumeración OLE estándar y se implementa de la manera habitual. No obstante, recuerde que el valor de PIDL que se devuelve debe ser relativo a la carpeta y contener solo la estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) del objeto y un terminador.

## <a name="implementing-the-optional-interfaces"></a>Implementar las interfaces opcionales

Hay una serie de interfaces de Shell opcionales que los objetos de carpeta de la extensión pueden admitir. Muchos de ellos, como [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona), le permiten personalizar distintos aspectos del modo en que el usuario ve la extensión. Otros, como [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), permiten que la extensión admita características como arrastrar y colocar.

Ninguna de las interfaces opcionales se expone directamente mediante un objeto de carpeta. En su lugar, el explorador de Windows llama a uno de los dos métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para solicitar una interfaz:

-   El explorador de Windows llama a [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) de un objeto de carpeta para solicitar una interfaz para uno de los objetos contenidos en la carpeta.
-   El explorador de Windows llama a [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) de un objeto de carpeta para solicitar una interfaz para la propia carpeta.

Para proporcionar la información, el objeto de carpeta crea un objeto que expone la interfaz solicitada y devuelve el puntero de interfaz. Después, el explorador de Windows llama a esa interfaz para recuperar la información necesaria. En esta sección se describen las interfaces opcionales que se usan con más frecuencia.

### <a name="iextracticon"></a>IExtractIcon

El explorador de Windows solicita una interfaz [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) antes de mostrar el contenido de una carpeta. La interfaz permite que la extensión especifique iconos personalizados para los objetos que contiene la carpeta. De lo contrario, se usarán los iconos de archivo y carpeta estándar. Para proporcionar un icono personalizado, cree un objeto de extracción de icono que exponga **IExtractIcon** y devuelva un puntero a esa interfaz. Para obtener más información, consulte la documentación de referencia de **IExtractIcon** o [creación de controladores de iconos](./how-to-create-icon-handlers.md).

### <a name="icontextmenu"></a>IContextMenu

Cuando un usuario hace clic con el botón secundario en un objeto, el explorador de Windows solicita una interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Para proporcionar menús contextuales para los objetos, cree un objeto de controlador de menú y devuelva su interfaz **IContextMenu** .

Los procedimientos para crear un objeto de controlador de menú son muy similares a los que se usan para crear una extensión de Shell de controlador de menú. Para obtener más información, vea [crear controladores de menús contextuales](context-menu-handlers.md) o la referencia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)o [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) .

### <a name="iqueryinfo"></a>IQueryInfo

El explorador de Windows llama a la interfaz [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) para recuperar una cadena de texto informativa.

### <a name="idataobject-and-idroptarget"></a>IDataObject e IDropTarget

Cuando el explorador de Windows muestra los objetos, un objeto de carpeta no tiene ninguna forma directa de saber cuándo un usuario está intentando cortar, copiar o arrastrar un objeto. En su lugar, el explorador de Windows solicita una interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Para permitir la transferencia del objeto, cree un objeto de datos y devuelva un puntero a su interfaz **IDataObject** .

Del mismo modo, un usuario podría intentar quitar un objeto de datos en una representación del explorador de Windows de uno de los objetos, como un icono o una ruta de acceso de la barra de direcciones. Después, el explorador de Windows solicita una interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Para permitir quitar el objeto de datos, cree un objeto que exponga una interfaz **IDropTarget** y devuelva el puntero de interfaz.

Controlar la transferencia de datos es uno de los aspectos más complicados de escribir extensiones de espacio de nombres. Para obtener una explicación detallada, vea [transferir objetos de Shell con arrastrar y colocar y el portapapeles](dragdrop.md).

## <a name="working-with-the-default-shell-folder-view-implementation"></a>Trabajar con la implementación de vista de carpeta de Shell predeterminada

Los orígenes de datos que usan el objeto de vista de carpeta de shell predeterminado (DefView) deben implementar estas interfaces:

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

Opcionalmente, también pueden implementar [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3).

 

 
