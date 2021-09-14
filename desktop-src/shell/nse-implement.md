---
description: El procedimiento para implementar una extensión de espacio de nombres es similar al de cualquier otro objeto del Modelo de objetos componentes (COM) en proceso.
title: Implementar las interfaces básicas de objetos de carpeta
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267839"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>Implementar las interfaces básicas de objetos de carpeta

El procedimiento para implementar una extensión de espacio de nombres es similar al de cualquier otro objeto del Modelo de objetos componentes (COM) en proceso. Todas las extensiones deben admitir tres interfaces principales que proporcionen a Windows Explorer la información básica necesaria para mostrar las carpetas de la extensión en la vista de árbol. Sin embargo, para hacer un uso completo de las funcionalidades del Explorador de Windows, la extensión también debe exponer una o varias interfaces opcionales que admitan características más sofisticadas, como menús contextuales o arrastrar y colocar, y proporcionar una vista de carpeta.

En este documento se describe cómo implementar las interfaces principal y opcional que Windows Explorer solicita información sobre el contenido de la extensión. Para obtener una explicación de cómo implementar una vista de carpeta y cómo personalizar Windows Explorer, vea [Implementing a Folder View](../lwef/nse-folderview.md).

-   [Implementación y registro básicos](#basic-implementation-and-registration)
    -   [Registro de una extensión](#registering-an-extension)
-   [Control de PIDL](#handling-pidls)
    -   [Creación de una estructura DEDABA](#creating-an-shitemid-structure)
    -   [Construcción de un PIDL](#constructing-a-pidl)
    -   [Interpretación de PIDL](#interpreting-pidls)
-   [Implementación de las interfaces principales](#implementing-the-primary-interfaces)
    -   [IPersistFolder (interfaz)](#ipersistfolder-interface)
    -   [IShellFolder (interfaz)](#ishellfolder-interface)
    -   [IEnumIDList (Interfaz)](#ienumidlist-interface)
-   [Implementar las interfaces opcionales](#implementing-the-optional-interfaces)
    -   [IExtractIcon](#iextracticon)
    -   [IContextMenu](#icontextmenu)
    -   [IQueryInfo](#iqueryinfo)
    -   [IDataObject e IDropTarget](#idataobject-and-idroptarget)
-   [Trabajar con la implementación de vista de carpeta de Shell predeterminada](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>Implementación y registro básicos

Como servidor COM en proceso, el archivo DLL debe exponer varias funciones e interfaces estándar:

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Estas funciones e interfaces se implementan de la misma manera que para la mayoría de los demás objetos COM. Para obtener más información, consulte la [documentación de COM](../com/the-component-object-model.md).

### <a name="registering-an-extension"></a>Registro de una extensión

Al igual que con todos los objetos COM, debe crear un GUID de identificador de clase (CLSID) para la extensión. Registre el objeto mediante la creación de una subclave **de HKEY \_ CLASSES \_ ROOT** \\ **CLSID** denominada para el CLSID de la extensión. El archivo DLL debe registrarse como un servidor en proceso y debe especificar el modelo de subprocesos de apartamento. Puede personalizar el comportamiento de la carpeta raíz de una extensión agregando una variedad de subclaves y valores a la clave CLSID de la extensión.

Algunos de estos valores solo se aplican a las extensiones con puntos de unión virtuales. Estos valores no se aplican a las extensiones cuyos puntos de unión son carpetas del sistema de archivos. Para obtener más información, vea Especificar la ubicación de [una extensión de espacio de nombres.](nse-junction.md) Para modificar el comportamiento de una extensión con un punto de unión virtual, agregue uno o varios de los valores siguientes a la clave CLSID de la extensión:

-   QuiereFORPARSING. El nombre de análisis de una extensión con un punto de unión virtual normalmente tendrá el formato ::{*GUID*}. Las extensiones de este tipo normalmente contienen elementos virtuales. Sin embargo, algunas extensiones, como Mis documentos, se corresponden realmente con las carpetas del sistema de archivos, aunque tengan puntos de unión virtuales. Si la extensión representa objetos del sistema de archivos de esta manera, puede establecer el valor WantsFORPARSING. Windows A continuación, el Explorador solicitará el nombre de análisis de la carpeta raíz llamando al método [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) del objeto de carpeta con *uFlags* establecido en **SHGDN \_ FORPARSING** y *pidl* establecido en un único puntero vacío a una lista de identificadores de elemento (PIDL). Un PIDL vacío solo contiene un terminador. A continuación, el método debe devolver el nombre de análisis ::{*GUID*} de la carpeta raíz.
-   HideFolderVerbs. Los verbos registrados en **la carpeta RAÍZ HKEY \_ CLASSES \_** normalmente están \\  asociados a todas las extensiones. Aparecen en el menú contextual de la extensión y [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)los puede invocar. Para evitar que cualquiera de estos verbos se asocie a la extensión, establezca el valor hideFolderVerbs.
-   HideAsDelete. Si un usuario intenta eliminar la extensión, Windows Explorador ocultará la extensión.
-   HideAsDeletePerUser. Este valor tiene el mismo efecto que HideAsDelete, pero por usuario. La extensión solo está oculta para los usuarios que han intentado eliminarla. La extensión es visible para todos los demás usuarios.
-   QueryForOverlay. Establezca este valor para indicar que el icono de la carpeta raíz puede tener una superposición de iconos. El objeto de carpeta debe admitir la [**interfaz IShellIconOverlay.**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) Antes de Windows Explorer muestre el icono de la carpeta raíz, solicitará un icono de superposición llamando a uno de los dos métodos **IShellIconOverlay** con *pidlItem* establecido en un PIDL vacío.

Los valores y subclaves restantes se aplican a todas las extensiones:

-   Para especificar el nombre para mostrar de la carpeta de punto de unión de la extensión, establezca el valor predeterminado de la subclave CLSID de la extensión en una cadena adecuada.
-   Cuando el cursor mantiene el puntero sobre una carpeta, normalmente se muestra una información detallada que describe el contenido de la carpeta. Para proporcionar información sobre la carpeta raíz de la extensión, cree un valor **REG \_ SZ** de InfoTip para la clave CLSID de la extensión y establízcalo en una cadena adecuada.
-   Para especificar un icono personalizado para la carpeta raíz de la extensión, cree una subclave de la subclave CLSID de la extensión denominada **DefaultIcon**. Establezca el valor predeterminado **de DefaultIcon** en un valor **REG \_ SZ** que contenga el nombre del archivo que contiene el icono, seguido de una coma, seguido de un signo menos, seguido del índice del icono en ese archivo.
-   De forma predeterminada, el menú contextual de la carpeta raíz de la extensión contendrá los elementos definidos en la carpeta **RAÍZ HKEY \_ CLASSES \_ \\**. Los **elementos Eliminar**  , **Cambiar** nombre y Propiedades se agregan si ha establecido las marcas SFGAO \_ XXX adecuadas. Puede agregar otros elementos al menú contextual de la carpeta raíz o invalidar los elementos existentes, como haría para un [tipo de archivo](fa-file-types.md). Cree una **subclave** de Shell bajo la clave CLSID de la extensión y defina comandos como se describe en [Extensión de menús contextuales](context.md).
-   Si necesita una manera más flexible de controlar el menú contextual de la carpeta raíz, puede implementar un controlador [de menú contextual](context-menu-handlers.md). Para registrar el controlador del menú contextual, cree una **tecla ShellEx** en la clave CLSID de la extensión. Registre el CLSID del controlador como lo haría para crear controladores de [extensión de shell convencionales.](handlers.md)
-   Para agregar una página a la hoja de propiedades de propiedades de la carpeta raíz, dé a la carpeta el atributo **\_ SFGAO HASPROPSHEET** e implemente un controlador [de hoja de propiedades](propsheet-handlers.md). Para registrar el controlador de la hoja de propiedades, cree una **clave ShellEx** en la clave CLSID de la extensión. Registre el CLSID del controlador como lo haría para crear controladores de [extensión de shell convencionales.](handlers.md)
-   Para especificar los atributos de la carpeta raíz, agregue una **subclave ShellFolder** a la subclave CLSID de la extensión. Cree un valor Atributos y estagúdelo en la combinación adecuada de [**marcas \_ SFGAO XXX.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)

En la tabla siguiente se enumeran algunos atributos que se usan habitualmente para las carpetas raíz.



| Marca                | Value      | Descripción                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CARPETA \_ SFGAO       | 0x20000000 | La carpeta raíz de la extensión contiene uno o varios elementos.                                                                                                                                                                                                                                                           |
| SFGAO \_ HASSUBFOLDER | 0x80000000 | La carpeta raíz de la extensión contiene una o varias subcarpetas. Windows El Explorador colocará un signo más ( + ) junto al icono de carpeta.                                                                                                                                                                               |
| SFGAO \_ CANDELETE    | 0x00000020 | El usuario puede eliminar la carpeta raíz de la extensión. El menú contextual de la carpeta tendrá un **elemento Eliminar.** Esta marca debe establecerse para los puntos de unión que se colocan en una de las [carpetas virtuales](nse-junction.md).                                                                                 |
| SFGAO \_ CANRENAME    | 0x00000010 | El usuario puede cambiar el nombre de la carpeta raíz de la extensión. El menú contextual de la carpeta tendrá un elemento **Cambiar** nombre.                                                                                                                                                                                                   |
| SFGAO \_ HASPROPSHEET | 0x00000040 | La carpeta raíz de la extensión tiene una **hoja de propiedades** Propiedades. El menú contextual de la carpeta tendrá un **elemento** Propiedades. Para proporcionar la hoja de propiedades, debe implementar un controlador [de hoja de propiedades](propsheet-handlers.md). Registre el controlador en la clave CLSID de la extensión, como se ha analizado anteriormente. |



 

En el ejemplo siguiente se muestra la entrada del Registro CLSID para una extensión con el nombre para mostrar MyExtension. La extensión tiene un icono personalizado que se encuentra en el archivo DLL de la extensión con un índice de 1. Se **establecen los atributos \_ SFGAO FOLDER**, **SFGAO \_ HASSUBFOLDER** y **SFGAO \_ CANDELETE.**

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

## <a name="handling-pidls"></a>Control de PIDL

Cada elemento del espacio de nombres de Shell debe tener un PIDL único. Windows El Explorador asigna un PIDL a la carpeta raíz y pasa el valor a la extensión durante la inicialización. A continuación, la extensión es responsable de asignar un PIDL construido correctamente a cada uno de sus objetos y proporcionar esos PIDL a Windows Explorer a petición. Cuando el shell usa un PIDL para identificar uno de los objetos de la extensión, la extensión debe ser capaz de interpretar el PIDL e identificar el objeto concreto. La extensión también debe asignar un [**nombre para mostrar**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) y un nombre de *análisis* a cada objeto. Dado que las PIDL las usan prácticamente todas las interfaces de carpetas, las extensiones normalmente implementan un único administrador *de PIDL* para controlar todas estas tareas.

El término PIDL es corto para una [**estructura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o un puntero a dicha estructura, en función del contexto. Tal y como se declara, **una estructura ITEMIDLIST** tiene un único miembro, [**una estructura DESUSOD.**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) La estructura **ITEMIDLIST de** un objeto es en realidad una matriz empaquetada de dos o más estructuras **DESUSOD.** El orden de estas estructuras define una ruta de acceso a través del espacio de nombres, de la misma manera que c: MyDirectory MyFile define una ruta de acceso a través \\ \\ del sistema de archivos. Por lo general, el PIDL de un objeto constará de una serie de estructuras **DE DESDUSEADAS** que se corresponden con las carpetas que definen la ruta de acceso del espacio de nombres, seguidas de la estructura **DESMID** DEL objeto, seguida de un terminador.

El terminador es una [**estructura DESMITED,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) con el *miembro cb* establecido en **NULL.** El terminador es necesario porque el número de estructuras **DESUSOMID** del PIDL de un objeto depende de la ubicación del objeto en el espacio de nombres shell y del punto inicial de la ruta de acceso. Además, el tamaño de las distintas estructuras **DESENLAZADAS** puede variar. Cuando recibe un PIDL, no tiene ninguna manera sencilla de determinar su tamaño o incluso el número total de estructuras **DESASEMITAD.** En su lugar, debe "recorrer" la matriz empaquetada, estructura por estructura, hasta llegar al terminador.

Para crear un PIDL, la aplicación debe:

1.  Cree una [**estructura DEDABADO**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para cada uno de sus objetos.
2.  Ensamble las [**estructuras DE DESENLAZ**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) pertinentes en un PIDL.

### <a name="creating-an-shitemid-structure"></a>Creación de una estructura DEDABA

La estructura [**DESTEMINADO de**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) un objeto identifica de forma única el objeto dentro de su carpeta. De hecho, un tipo de PIDL utilizado por muchos de los métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) consta solo de la estructura **DESMITED del** objeto, seguida de un terminador. La definición de **una estructura DESMID** ES:


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



El *miembro abID* es el identificador del objeto. Dado que la longitud de *abID* no está definida y puede variar, el *miembro cb* se establece en el tamaño de la estructura [**DESUSOD,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) en bytes.

Dado que ni la longitud ni el contenido de *abID* están estandarizados, puede usar cualquier esquema que desee asignar valores *abID* a los objetos. El único requisito es que no se puedan tener dos objetos en la misma carpeta con valores idénticos. Sin embargo, por motivos de rendimiento, [**la estructura DESENLAZTED**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) debe estar **alineada con DWORD.** En otras palabras, debe construir los valores *abID* de modo que *cb* sea un múltiplo entero de 4.

Normalmente, *abID* apunta a una estructura definida por la extensión. Además del identificador del objeto, esta estructura se usa a menudo para contener una variedad de información relacionada, como el tipo o los atributos del objeto. Los objetos de carpeta de la extensión pueden extraer rápidamente la información del PIDL en lugar de tener que consultarla.

> [!Note]  
> Uno de los aspectos más importantes del diseño de una estructura de datos para un PIDL es hacer que la estructura sea persistente y transportable. En el contexto de las PIDL, el significado de estos términos es:
>
> -   Persistente. Con frecuencia, el sistema coloca los PIDL en varios tipos de almacenamiento a largo plazo, como los archivos de acceso directo. A continuación, puede recuperar estos PIDL del almacenamiento más adelante, posiblemente después de reiniciar el sistema. Un PIDL que se haya recuperado del almacenamiento debe seguir siendo válido y significativo para la extensión. Este requisito significa, por ejemplo, que no debe usar punteros ni identificadores en la estructura PIDL. Las PIDL que contienen este tipo de datos normalmente no tendrán sentido cuando el sistema los recupere más adelante del almacenamiento.
> -   Transportable. Un PIDL debe seguir siendo significativo cuando se transporte de un equipo a otro. Por ejemplo, un PIDL se puede escribir en un archivo de acceso directo, copiarse en un disquete y transportarse a otro equipo. Ese PIDL debe seguir siendo significativo para la extensión que se ejecuta en el segundo equipo. Por ejemplo, para asegurarse de que los PIDL son transportables, use explícitamente caracteres ANSI o Unicode. Evite tipos de datos **como TCHAR** **o LPTSTR.** Si usa esos tipos de datos, un PIDL creado en un equipo que ejecuta una versión Unicode de la extensión no podrá leerse mediante una versión ANSI de esa extensión que se ejecute en otro equipo.

 

En la declaración siguiente se muestra un ejemplo sencillo de una estructura de datos.


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



El **miembro cb** se establece en el tamaño de la estructura **MYPIDLDATA.** Este miembro hace **que MYPIDLDATA** sea una estructura [**DE DESMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) válida, en y de sí mismo. El resto de los miembros son equivalentes al **miembro abID** de una estructura **DESUSO Y** mantienen datos privados. El **miembro dwType** es un valor definido por la extensión que indica el tipo de objeto. En este ejemplo, **dwType se** establece en **TRUE para** carpetas y **FALSE** en caso contrario. Este miembro le permite, por ejemplo, determinar rápidamente si el objeto es una carpeta o no. El **miembro wszDisplayName** contiene el nombre para mostrar del objeto. Puesto que no asignaría el mismo nombre para mostrar a dos objetos diferentes de la misma carpeta, el nombre para mostrar también actúa como identificador de objeto. En este ejemplo, **wszDisplayName** se establece en 40 caracteres para garantizar que la estructura **DESENLAZMITE** será **DWORD**-aligned. Para limitar el tamaño de las PIDL, en su lugar puede usar una matriz de caracteres de longitud variable y ajustar el valor de cb en consecuencia. Repase la cadena de presentación con suficientes \\ caracteres "0" para mantener la alineación **DWORD** de la estructura. Otros miembros que pueden ser útiles para colocar en la estructura incluyen el tamaño del objeto, los atributos o el nombre del análisis.

### <a name="constructing-a-pidl"></a>Construcción de un PIDL

Una vez que haya definido las estructuras [**DE ESTAD para**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) los objetos, puede usarlas para construir un PIDL. Los PIDL se pueden construir para diversos propósitos, pero la mayoría de las tareas usan uno de los dos tipos de PIDL. El PIDL más sencillo, un PIDL de un solo nivel, identifica el objeto con respecto a su carpeta primaria. Muchos de los métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) usan este tipo de PIDL. Un PIDL de un solo nivel contiene la estructura **DESCONTROL DEL OBJETO,** seguida de un terminador. Un PIDL completo define una ruta de acceso a través de la jerarquía de espacios de nombres desde el escritorio hasta el objeto . Este tipo de PIDL se inicia en el escritorio y contiene una estructura **DE DESAESTE PARA CADA** carpeta de la ruta de acceso, seguida del objeto y el terminador. Un PIDL completo identifica de forma única el objeto dentro de todo el espacio de nombres de Shell.

La manera más sencilla de construir un PIDL es trabajar directamente con la propia [**estructura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Cree una **estructura ITEMIDLIST,** pero asigne suficiente memoria para contener todas las estructuras [**DE DESASIGNADAS.**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) La dirección de esta estructura apuntará a la estructura **INICIAL DESMID.** Defina los valores de los miembros de esta estructura inicial y, a continuación, anexe tantas estructuras **DE TIPO DE TRABAJO** adicionales como necesite, en el orden adecuado. En el procedimiento siguiente se describe cómo crear un PIDL de un solo nivel. Contiene dos estructuras **DE DESASEADAS:** **una estructura MYPIDLDATA** seguida de un terminador:

1.  Use la [**función CoTaskMemAlloc para**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar memoria para el PIDL. Asigne suficiente memoria para los datos privados más **un USHORT** (dos bytes) para el terminador. Convierte el resultado en LPMYPIDLDATA.
2.  Establezca el miembro cb de la primera **estructura MYPIDLDATA** en el tamaño de esa estructura. En este ejemplo, establecería **cb** en sizeof(MYPIDLDATA). Si desea usar una estructura de longitud variable, tendrá que calcular el valor de **cb**.
3.  Asigne los valores adecuados a los miembros de datos privados.
4.  Calcule la dirección de la siguiente [**estructura DE DESASEMITA.**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) Convierte la dirección de la estructura MYPIDLDATA actual en LPBYTE y agrega ese valor al valor **de cb** determinado en el paso 3.
5.  En este caso, la siguiente estructura [**DESMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) es el terminador. Establezca el miembro cb de **la estructura** en cero.

En el caso de los PIDL más largos, asigne memoria suficiente y repita los pasos del 3 al 5 para cada estructura [**DESASIGNADA**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) adicional.

La siguiente función de ejemplo toma el tipo y el nombre para mostrar de un objeto y devuelve el PIDL de un solo nivel del objeto. La función supone que el nombre para  mostrar, incluido su carácter nulo de terminación, no supera el número de caracteres declarados para la **estructura MYPIDLDATA.** Si esa suposición resulta errónea, la [**función StringCbCopyW**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) truncará el nombre para mostrar. La **variable \_ g pMalloc** es un [**puntero IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) creado en otro lugar y almacenado en una variable global.


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



Un PIDL completo debe tener estructuras [**DE LUGARD PARA**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) CADA objeto desde el escritorio hasta el objeto. La extensión recibe un PIDL completo para la carpeta raíz cuando el shell llama a [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize). Para construir un PIDL completo para un objeto, tome el PIDL que el shell ha asignado a la carpeta raíz y anexe las estructuras **DE LAEDED** NECESARIAS para llevarle desde la carpeta raíz al objeto .

### <a name="interpreting-pidls"></a>Interpretación de PIDL

Cuando el Shell o una aplicación llama a una de las interfaces de la extensión para solicitar información sobre un objeto, normalmente identificará el objeto mediante un PIDL. Algunos métodos, como [**IShellFolder::GetUIObjectOf,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)usan PIDL relativos a la carpeta primaria y son fáciles de interpretar. Sin embargo, es probable que la extensión también reciba pidls completos. A continuación, el administrador de PIDL debe determinar a qué objetos hace referencia PIDL.

Lo que complica la tarea de asociar un objeto a un PIDL completo es que una o varias de las estructuras [**iniciales DE ASEQD**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) iniciales de PIDL podrían pertenecer a objetos que se encuentran fuera de la extensión en el espacio de nombres shell. No tiene ninguna manera de interpretar el significado del *miembro abID* de esas estructuras. Lo que debe hacer la extensión es "recorrer" la lista de estructuras **DE LAVD,** hasta llegar a la estructura que corresponde a la carpeta raíz. A partir de ese momento, sabrá cómo interpretar la información en las estructuras **DE LADMEDA.**

Para recorrer el PIDL, tome el primer valor *cb* y agrégalo a la dirección del PIDL para avanzar el puntero al inicio de la siguiente estructura [**DESANGRED.**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) A continuación, apuntará al miembro *cb* de esa estructura, que se puede usar para avanzar el puntero al inicio de la siguiente estructura **DE LA ESTRUCTURA DE LA PROPIEDAD,** y así sucesivamente. Cada vez que avance el puntero, examine la **estructura DE LA ESTRUCTURA DE LA EXTENSIÓN PARA** determinar si ha alcanzado la raíz del espacio de nombres de la extensión.

## <a name="implementing-the-primary-interfaces"></a>Implementar las interfaces principales

Al igual que con todos los objetos COM, la implementación de una extensión es en gran medida una cuestión de implementar una colección de interfaces. En esta sección se de abordan las tres interfaces principales que todas las extensiones deben implementar. Se usan para la inicialización y para proporcionar Windows Explorer con información básica sobre el contenido de la extensión. Estas interfaces, además de una [vista de carpeta,](../lwef/nse-folderview.md)son todas las necesarias para una extensión funcional. Sin embargo, para aprovechar completamente las características de Windows Explorer, la mayoría de las extensiones también implementan una o varias de las interfaces opcionales.

### <a name="ipersistfolder-interface"></a>IPersistFolder (interfaz)

Se llama a la interfaz [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) para inicializar un nuevo objeto de carpeta. El [**método IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) asigna un PIDL completo al nuevo objeto . Almacene este PIDL para su uso posterior. Por ejemplo, un objeto de carpeta debe usar este PIDL para construir PIDL completos para los secundarios del objeto. El creador del objeto de carpeta también puede llamar a [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) para solicitar el CLSID del objeto.

Normalmente, el método [**IShellFolder::BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) de su carpeta primaria crea e inicializa un objeto de carpeta. Sin embargo, cuando un usuario examina la extensión, Windows Explorer crea e inicializa el objeto de carpeta raíz de la extensión. El PIDL que recibe el objeto de carpeta raíz a través de [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) contiene la ruta de acceso del escritorio a la carpeta raíz que necesitará para construir PIDL completos para la extensión.

### <a name="ishellfolder-interface"></a>Interfaz IShellFolder

Shell trata una extensión como una colección ordenada jerárquicamente de objetos de carpeta. La [**interfaz IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) es el núcleo de cualquier implementación de extensión. Representa un objeto de carpeta y proporciona Windows Explorer con gran parte de la información necesaria para mostrar el contenido de la carpeta.

[**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) suele ser la única interfaz de carpeta que no sea [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) expuesta directamente por un objeto de carpeta. Aunque Windows Explorer usa una variedad de interfaces obligatorias y opcionales para obtener información sobre el contenido de la carpeta, obtiene punteros a esas interfaces a través de **IShellFolder**.

Windows El Explorador obtiene el CLSID de la carpeta raíz de la extensión de varias maneras. Para obtener más información, vea [Especificar la ubicación](nse-junction.md) de una extensión de espacio de nombres o Mostrar una Self-Contained de una extensión de espacio de [nombres](nse-view.md). Windows A continuación, el Explorador usa ese CLSID para crear e inicializar una instancia de la carpeta raíz y consultar una [**interfaz IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) La extensión crea un objeto de carpeta para representar la carpeta raíz y devuelve la interfaz **IShellFolder del** objeto. Gran parte del resto de la interacción entre la extensión y Windows Explorer se realiza a través de **IShellFolder**. Windows El explorador llama **a IShellFolder** para:

-   Solicite un objeto que pueda enumerar el contenido de la carpeta raíz.
-   Obtenga varios tipos de información sobre el contenido de la carpeta raíz.
-   Solicite un objeto que exponga una de las interfaces opcionales. A continuación, se pueden consultar esas interfaces para obtener información adicional, como iconos o menús contextuales.
-   Solicite un objeto de carpeta que represente una subcarpeta de la carpeta raíz.

Cuando un usuario abre una subcarpeta de la carpeta raíz, Windows Explorer llama a [**IShellFolder::BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject). La extensión crea e inicializa un nuevo objeto de carpeta para representar la subcarpeta y devuelve su [**interfaz IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Windows A continuación, el Explorador llama a esta interfaz para varios tipos de información, y así sucesivamente hasta que el usuario decide navegar por otro lugar en el espacio de nombres shell o cerrar Windows Explorer.

En el resto de esta sección se analizan brevemente los métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) más importantes y cómo implementarlos.

### <a name="enumobjects"></a>EnumObjects

Antes de mostrar el contenido de una carpeta en la vista de árbol, Windows Explorer debe determinar primero qué contiene la carpeta llamando al método [**IShellFolder::EnumObjects.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) Este método crea un objeto de enumeración OLE estándar que expone una [**interfaz IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) y devuelve ese puntero de interfaz. La **interfaz IEnumIDList** permite a Windows Explorer obtener los PIDL de todos los objetos contenidos en la carpeta. A continuación, estos PIDL se usan para obtener información sobre los objetos contenidos en la carpeta . Para obtener más información, vea [IEnumIDList (Interfaz).](#ienumidlist-interface)

> [!Note]  
> El [**método IEnumIDList::Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) solo debe devolver los PIDL relativos a la carpeta primaria. El PIDL solo debe contener la estructura [**DE LA ESTRUCTURA DEL OBJETO, seguida**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de un terminador.

 

### <a name="createviewobject"></a>CreateViewObject

Antes de mostrar el contenido de una carpeta, Windows Explorer llama a este método para solicitar un puntero a una [**interfaz IShellView.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) Esta interfaz la usa Windows Explorer para administrar la vista de carpeta. Cree un objeto de vista de carpeta y devuelva su **interfaz IShellView.**

También se llama al método [**IShellFolder::CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) para solicitar una de las interfaces opcionales, como [**IContextMenu,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)para la propia carpeta. La implementación de este método debe crear un objeto que exponga la interfaz solicitada y devuelva el puntero de interfaz. Si Windows Explorer necesita una interfaz opcional para uno de los objetos contenidos en la carpeta , llamará a [**IShellFolder::GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof).

### <a name="getuiobjectof"></a>GetUIObjectOf

Aunque la información básica sobre el contenido de una carpeta está disponible a través de los métodos [**IShellFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) la extensión también puede proporcionar a Windows Explorer varios tipos de información adicional. Por ejemplo, puede especificar iconos para el contenido de una carpeta o del menú contextual de un objeto. Windows El explorador llama [**al método IShellFolder::GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) para intentar recuperar información adicional sobre un objeto contenido en una carpeta. Windows El Explorador especifica para qué objeto desea obtener la información y el IID de la interfaz correspondiente. A continuación, el objeto de carpeta crea un objeto que expone la interfaz solicitada y devuelve el puntero de interfaz.

Si la extensión permite a los usuarios transferir objetos con arrastrar y colocar o el Portapapeles, el Explorador de Windows llamará a [**IShellFolder::GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) para solicitar una interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) o [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) Para obtener más información, vea [Transferencia de objetos de shell con arrastrar y colocar y el Portapapeles.](dragdrop.md)

Windows El explorador [**llama a IShellFolder::CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) cuando quiere el mismo tipo de información sobre la propia carpeta.

### <a name="bindtoobject"></a>BindToObject

Windows El explorador llama [**al método IShellFolder::BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) cuando un usuario intenta abrir una de las subcarpetas de la extensión. Si *riid se* establece en IID IShellFolder, debe crear e inicializar un objeto de carpeta que represente la subcarpeta y devuelva la interfaz \_ [**IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) objeto.

> [!Note]  
> En la actualidad, Windows Explorer llama a este método solo para solicitar una [**interfaz IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Sin embargo, no suponga que este siempre será el caso. Siempre debe comprobar el valor de *riid* antes de continuar.

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

Windows El explorador llama [**al método IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para convertir el PIDL de uno de los objetos de la carpeta en un nombre. Ese PIDL debe ser relativo a la carpeta primaria del objeto. En otras palabras, debe contener una única estructura NO **NULL** [**DE LA ESTRUCTURA DE LA PROPIEDAD DE LA PROPIEDAD.**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) Dado que hay más de una manera posible de dar nombre a los objetos, Windows Explorer especifica el tipo de nombre estableciendo una o varias marcas [**SHGDNF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf) en el parámetro *uFlags.* Uno de los dos valores, **SHGDN \_ NORMAL** o **SHGDN \_ INFOLDER,** se establecerá para especificar si el nombre debe ser relativo a la carpeta o relativo al escritorio. Uno de los otros tres valores, **SHGDN \_ FOREDITING,** **SHGDN \_ FORADDRESSBAR** o **SHGDN \_ FORPARSING,** se puede establecer para especificar para qué se usará el nombre.

Debe devolver el nombre en forma de una [**estructura STRRET.**](/windows/desktop/api/Shtypes/ns-shtypes-strret) Si **SHGDN \_ FOREDITING,** **SHGDN \_ FORADDRESSBAR** y **SHGDN \_ FORPARSING** no están establecidos, devuelva el nombre para mostrar del objeto. Si se establece la marca **SHGDN \_ FORPARSING,** Windows Explorer solicita un nombre de análisis. El análisis de nombres se pasa a [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) para obtener el PIDL de un objeto, aunque podría encontrarse uno o varios niveles por debajo de la carpeta actual en la jerarquía de espacios de nombres. Por ejemplo, el nombre de análisis de un objeto del sistema de archivos es su ruta de acceso. Puede pasar la ruta de acceso completa de cualquier objeto del sistema de archivos al método **IShellFolder::P arseDisplayName** del escritorio y devolverá el PIDL completo del objeto.

Aunque los nombres de análisis son cadenas de texto, no necesariamente tienen que incluir el nombre para mostrar. Debe asignar nombres de análisis en función de lo que funcionará de forma más eficaz cuando se llame a [**IShellFolder::P arseDisplayName.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) Por ejemplo, muchas de las carpetas virtuales del shell no forman parte del sistema de archivos y no tienen una ruta de acceso completa. En su lugar, a cada carpeta se le asigna un GUID y el nombre del análisis tiene la forma ::{GUID}. Independientemente del esquema que use, debería poder realizar un "recorrido de ida y vuelta" de forma confiable. Por ejemplo, si un autor de la llamada pasa un nombre de análisis a **IShellFolder::P arseDisplayName** para recuperar el PIDL de un objeto y, a continuación, pasa ese PIDL a [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) con la marca **SHGDN \_ FORPARSING** establecida, el autor de la llamada debe recuperar el nombre de análisis original.

### <a name="getattributesof"></a>GetAttributesOf

Windows El explorador llama [**al método IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) para determinar los atributos de uno o varios elementos contenidos en un objeto de carpeta. El valor de *cidl* proporciona el número de elementos de la consulta y *aPidl* apunta a una lista de sus PIDL.

Dado que las pruebas de algunos atributos pueden llevar mucho tiempo, Windows Explorer normalmente restringe la consulta a un subconjunto de las marcas disponibles estableciendo sus valores en *rfgInOut*. El método debe probar solo los atributos cuyas marcas se establecen en *rfgInOut*. Deje establecidas las marcas válidas y borre el resto. Si se incluye más de un elemento en la consulta, establezca solo las marcas que se aplican a todos los elementos.

> [!Note]  
> Los atributos deben establecerse correctamente para que un elemento se muestre correctamente. Por ejemplo, si un elemento es una carpeta que contiene subcarpetas, debe establecer la marca **\_ SFGAO HASSUBFOLDER.** De lo Windows explorador no mostrará un signo + junto al icono del elemento en la vista de árbol.

 

### <a name="parsedisplayname"></a>ParseDisplayName

El [**método IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) es en cierto sentido una imagen reflejada de [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). El uso más común de este método es convertir el nombre de análisis de un objeto en el PIDL asociado. El nombre del análisis puede hacer referencia a cualquier objeto que se encuentra debajo de la carpeta en la jerarquía de espacios de nombres. El PIDL devuelto es relativo al objeto de carpeta que expone el método y normalmente no está completo. En otras palabras, aunque el PIDL puede contener varias estructuras [**DESATENTARD,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) la primera será la del propio objeto o la primera subcarpeta de la ruta de acceso de la carpeta al objeto. El autor de la llamada tendrá que anexar este PIDL al PIDL completo de la carpeta para obtener un PIDL completo para el objeto.

[**También se puede llamar a IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) para solicitar los atributos de un objeto. Dado que determinar todos los atributos aplicables puede llevar mucho tiempo, el autor de la llamada establecerá solo las marcas XXX de [**SFGAO \_**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) que representan la información en la que está interesado el autor de la llamada. Debe determinar cuál de esos atributos es true para el objeto y borrar las marcas restantes.

### <a name="ienumidlist-interface"></a>IEnumIDList (Interfaz)

Cuando Windows explorer necesita enumerar los objetos contenidos en una carpeta, llama a [**IShellFolder::EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects). El objeto de carpeta debe crear un objeto de enumeración que exponga la [**interfaz IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) y devuelva ese puntero de interfaz. Windows A continuación, el explorador usará **normalmente IEnumIDList** para enumerar los PIDL de todos los objetos contenidos en la carpeta .

[**IEnumIDList es**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) una interfaz de enumeración OLE estándar y se implementa de la manera habitual. No obstante, recuerde que las PIDL que devuelve deben ser relativas a la carpeta y contener solo la estructura [**DESMITED**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) del objeto y un terminador.

## <a name="implementing-the-optional-interfaces"></a>Implementar las interfaces opcionales

Hay varias interfaces de Shell opcionales que los objetos de carpeta de la extensión pueden admitir. Muchos de ellos, como [**IExtractIcon,**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)permiten personalizar varios aspectos de la forma en que el usuario ve la extensión. Otros, como [**IDataObject,**](/windows/win32/api/objidl/nn-objidl-idataobject)permiten que la extensión admita características como arrastrar y colocar.

Ninguna de las interfaces opcionales se expone directamente mediante un objeto de carpeta. En su lugar, Windows explorer llama a uno de los dos métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para solicitar una interfaz:

-   Windows El Explorador llama a [**IShellFolder::GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) de un objeto de carpeta para solicitar una interfaz para uno de los objetos contenidos en la carpeta.
-   Windows El Explorador llama a [**IShellFolder::CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) de un objeto de carpeta para solicitar una interfaz para la propia carpeta.

Para proporcionar la información, el objeto de carpeta crea un objeto que expone la interfaz solicitada y devuelve el puntero de interfaz. Windows A continuación, el Explorador llama a esa interfaz para recuperar la información necesaria. En esta sección se de abordan las interfaces opcionales que se usan con más frecuencia.

### <a name="iextracticon"></a>IExtractIcon

Windows El explorador solicita una [**interfaz IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) antes de mostrar el contenido de una carpeta. La interfaz permite que la extensión especifique iconos personalizados para los objetos contenidos en la carpeta . De lo contrario, se usarán los iconos estándar de archivos y carpetas. Para proporcionar un icono personalizado, cree un objeto de extracción de iconos que exponga **IExtractIcon** y devuelva un puntero a esa interfaz. Para obtener más información, vea la documentación **de referencia de IExtractIcon** o [Crear controladores de iconos](./how-to-create-icon-handlers.md).

### <a name="icontextmenu"></a>IContextMenu

Cuando un usuario hace clic con el botón derecho en un objeto, Windows Explorer solicita una [**interfaz IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Para proporcionar menús contextuales para los objetos, cree un objeto de controlador de menús y devuelva su **interfaz IContextMenu.**

Los procedimientos para crear un objeto de controlador de menús son muy similares a los que se usan para crear una extensión shell del controlador de menús. Para obtener más información, vea [Crear controladores de menú contextual](context-menu-handlers.md) o la referencia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) [**o IContextMenu3.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)

### <a name="iqueryinfo"></a>IQueryInfo

Windows El Explorador llama a [**la interfaz IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) para recuperar una cadena de texto de información.

### <a name="idataobject-and-idroptarget"></a>IDataObject e IDropTarget

Cuando el Explorador de Windows muestra los objetos, un objeto de carpeta no tiene ninguna manera directa de saber cuándo un usuario intenta cortar, copiar o arrastrar un objeto. En su lugar, Windows Explorer solicita una [**interfaz IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject) Para permitir la transferencia del objeto, cree un objeto de datos y devuelva un puntero a su **interfaz IDataObject.**

De forma similar, un usuario podría intentar quitar un objeto de datos en una representación de Windows Explorer de uno de los objetos, como un icono o una ruta de acceso de la barra de direcciones. Windows A continuación, el Explorador solicita [**una interfaz IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) Para permitir que se pueda descartar el objeto de datos, cree un objeto que exponga una **interfaz IDropTarget** y devuelva el puntero de interfaz.

El control de la transferencia de datos es uno de los aspectos más complicados de escribir extensiones de espacio de nombres. Para obtener una explicación detallada, vea Transferencia de objetos de shell con arrastrar [y colocar y el Portapapeles.](dragdrop.md)

## <a name="working-with-the-default-shell-folder-view-implementation"></a>Trabajar con la implementación de vista de carpeta de Shell predeterminada

Los orígenes de datos que usan el objeto de vista de carpeta de Shell (DefView) predeterminado deben implementar estas interfaces:

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

Opcionalmente, también pueden implementar [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3).

 

 
