---
description: El objeto de datos es fundamental para todas las transferencias de datos del shell.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Objeto de datos de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812e5c18f5a2120fbf22682c6e768dc005128630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275238"
---
# <a name="shell-data-object"></a>Objeto de datos de shell

El objeto de datos es fundamental para todas las transferencias de datos del shell. Es principalmente un contenedor que contiene los datos transferidos. Sin embargo, el destino también puede comunicarse con el objeto de datos para facilitar algunos tipos especializados de transferencia de datos de Shell, como los movimientos optimizados. En este tema se proporciona una explicación general de cómo funcionan los objetos de datos de Shell, cómo se construyen mediante un origen y cómo se administran mediante un destino. Para obtener una explicación detallada sobre cómo usar los objetos de datos para transferir distintos tipos de datos de Shell, vea [administrar escenarios de transferencia de datos de Shell](datascenarios.md).

-   [Cómo funcionan los objetos de datos](#how-data-objects-work)
    -   [Formatos del portapapeles](#clipboard-formats)
    -   [FORMATETC (estructura)](#formatetc-structure)
    -   [Estructura STGMEDIUM](#stgmedium-structure)
-   [Cómo crea un origen un objeto de datos](#how-a-source-creates-a-data-object)
    -   [Cómo agregar un objeto de memoria global a un objeto de datos](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementar IDataObject](#implementing-idataobject)
    -   [Implementación de IDropSource](#implementing-idropsource)
-   [Cómo controla un destino un objeto de datos](#how-a-target-handles-a-data-object)
    -   [Extraer datos de Shell de un objeto de datos](#extracting-shell-data-from-a-data-object)
    -   [Implementar IDropTarget](#implementing-idroptarget)
-   [Usar el objeto auxiliar de arrastrar y colocar](#using-the-drag-and-drop-helper-object)
    -   [Uso de la interfaz IDragSourceHelper](#using-the-idragsourcehelper-interface)
    -   [Usar la interfaz IDropTargetHelper](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Cómo funcionan los objetos de datos

Los objetos de datos son objetos del modelo de objetos componentes (COM), creados por el origen de datos para transferir datos a un destino. Normalmente llevan más de un elemento de datos. Hay dos razones para esta práctica:

-   Aunque casi cualquier tipo de datos se puede transferir con un objeto de datos, el origen normalmente no sabe qué tipo de datos puede aceptar el destino. Por ejemplo, los datos pueden ser una parte de un documento de texto con formato. Aunque es posible que el destino sea capaz de administrar información de formato complejo, también podría aceptar únicamente texto ANSI. Por este motivo, los objetos de datos suelen incluir los mismos datos en varios formatos diferentes. A continuación, el destino puede extraer los datos en un formato que pueda controlar.
-   Los objetos de datos también pueden contener elementos de datos auxiliares que no son versiones de datos de origen. Normalmente, este tipo de elemento de datos proporciona información adicional sobre la operación de transferencia de datos. Por ejemplo, el shell utiliza elementos de datos auxiliares para indicar si un archivo se va a copiar o quitar.

### <a name="clipboard-formats"></a>Formatos del portapapeles

Cada elemento de datos de un objeto de datos tiene un formato asociado, normalmente denominado *formato del portapapeles*. Hay una serie de formatos de Portapapeles estándar, declarados en Winuser. h, que corresponden a tipos de datos de uso frecuente. Los formatos del portapapeles son enteros, pero normalmente se hace referencia a ellos por su nombre equivalente, que tiene la forma CF \_ *XXX*. Por ejemplo, el formato del portapapeles para texto ANSI es el \_ texto CF.

Las aplicaciones pueden extender el intervalo de formatos de Portapapeles disponibles definiendo formatos privados. Para definir un formato privado, una aplicación llama a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) con una cadena que identifica el formato. El entero sin signo que devuelve la función es un valor de formato válido que se puede usar como un formato estándar del portapapeles. Sin embargo, tanto el origen como el destino deben registrar el formato para poder usarlo. Con una excepción:[CF \_ HDROP](clipboard.md): los formatos del portapapeles que se usan para transferir datos de Shell se definen como formatos privados. El origen y el destino deben registrarlos para poder usarlos. Para obtener una descripción de los formatos disponibles del portapapeles de Shell, consulte formatos del portapapeles de Shell.

Aunque hay algunas excepciones, los objetos de datos normalmente solo contienen un elemento de datos para cada formato del portapapeles que admiten. Esta correlación uno a uno entre el formato y los datos permite usar el valor de formato como identificador para el elemento de datos asociado. De hecho, al analizar el contenido de un objeto de datos, un elemento de datos determinado se denomina normalmente "formato" y se hace referencia a él mediante su nombre de formato. Por ejemplo, frases como "extraer el formato de \_ texto de CF..." normalmente se utilizan al discutir el elemento de datos de texto ANSI de un objeto de datos.

Cuando el destino de colocación recibe el puntero al objeto de datos, el destino de colocación enumera los formatos disponibles para determinar qué tipos de datos están disponibles. A continuación, solicita uno o más de los formatos disponibles y extrae los datos. La forma específica en que el destino extrae los datos de Shell de un objeto de datos varía con el formato; Esto se describe con más detalle en [cómo un destino controla un objeto de datos](#how-a-target-handles-a-data-object).

Con las transferencias de datos del portapapeles simples, los datos se colocan en un objeto de memoria global. La dirección de ese objeto se coloca en el portapapeles, junto con su formato. El formato del portapapeles indica al destino qué tipo de datos se va a encontrar en la dirección asociada. Mientras que las transferencias de Portapapeles simples son fáciles de implementar:

-   Los objetos de datos proporcionan una manera mucho más flexible de transferir datos.
-   Los objetos de datos son más adecuados para transferir grandes cantidades de datos.
-   Los objetos de datos se deben utilizar para transferir datos con una operación de arrastrar y colocar.

Por estos motivos, todas las transferencias de datos de Shell usan objetos de datos. Con los objetos de datos, los formatos del portapapeles no se utilizan directamente. En su lugar, los elementos de datos se identifican con una generalización del formato del portapapeles, una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) .

### <a name="formatetc-structure"></a>FORMATETC (estructura)

La estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) es una versión extendida de un formato de Portapapeles. Tal y como se usa para las transferencias de datos de Shell, la estructura **FORMATETC** tiene las siguientes características:

-   Un elemento de datos todavía se identifica mediante el formato del portapapeles, en el miembro **cfFormat** .
-   La transferencia de datos no se limita a los objetos de memoria global. El miembro **tymed** se usa para indicar el mecanismo de transferencia de datos contenido en la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) asociada. Se establece en uno de los valores de [**TYMED \_ XXX**](/windows/win32/api/objidl/ne-objidl-tymed) .
-   El shell usa el miembro **lIndex** con su formato [CFSTR \_ FILECONTENTS](clipboard.md) para permitir que un objeto de datos contenga más de un elemento de datos por cada formato. Para obtener una explicación de cómo usar este formato, vea la sección *usar el \_ formato CFSTR FILECONTENTS para extraer datos de un archivo* de [control de escenarios de transferencia de datos de Shell](datascenarios.md).
-   Normalmente, el miembro **dwAspect** se establece en DVASPECT \_ Content. Sin embargo, hay tres valores definidos en ShlObj. h que se pueden usar para la transferencia de datos de Shell. 

    |                     |                                                                                                   |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | copia de DVASPECT \_      | Se utiliza para indicar que el formato representa una copia de los datos.                                   |
    | vínculo a DVASPECT \_      | Se utiliza para indicar que el formato representa un acceso directo a los datos.                               |
    | DVASPECT \_ nombre_corto | Se usa con el \_ formato de CF HDROP para solicitar una ruta de acceso de archivo con los nombres acortados al formato 8,3. |

    

     

-   El miembro **PTD** no se utiliza para las transferencias de datos de Shell y, normalmente, se establece en **null**.

### <a name="stgmedium-structure"></a>Estructura STGMEDIUM

La estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) proporciona acceso a los datos que se van a transferir. Se admiten tres mecanismos de transferencia de datos para los datos de Shell:

-   Objeto de memoria global.
-   Interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) .
-   Una interfaz [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

El miembro **tymed** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) es un valor de [**tymed \_ XXX**](/windows/win32/api/objidl/ne-objidl-tymed) que identifica el mecanismo de transferencia de datos. El segundo miembro es un puntero que el destino usa para extraer los datos. El puntero puede ser uno de varios tipos, dependiendo del valor de **tymed** . Los tres valores de **tymed** que se usan para las transferencias de datos de Shell se resumen en la tabla siguiente, junto con el nombre de miembro de **STGMEDIUM** correspondiente.



| Valor tymed     | Nombre del miembro | Descripción                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **hGlobal** | Un puntero a un objeto de memoria global. Este tipo de puntero se usa normalmente para transferir pequeñas cantidades de datos. Por ejemplo, el shell utiliza objetos de memoria global para transferir cadenas de texto corto como nombres de archivo o direcciones URL.                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | Puntero a una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Este tipo de puntero es preferible para la mayoría de las transferencias de datos del shell porque requiere relativamente poca memoria en comparación con el \_ HGLOBAL TYMED. Además, el \_ mecanismo de transferencia de datos de TYMED ISTREAM no requiere que el origen almacene sus datos de una manera determinada. |
| TYMED \_ ISTORAGE | **pstg**    | Puntero a una interfaz [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . El destino llama a los métodos de interfaz para extraer los datos. Al igual que TYMED \_ ISTREAM, este tipo de puntero requiere relativamente poca memoria. Sin embargo, dado que TYMED \_ ISTORAGE es menos flexible que TYMED \_ ISTREAM, no se suele usar.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Cómo crea un origen un objeto de datos

Cuando un usuario inicia una transferencia de datos de Shell, el origen es responsable de crear un objeto de datos y de cargarlo con los datos. En el procedimiento siguiente se resume el proceso:

1.  Llame a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obtener un valor de formato de Portapapeles válido para cada formato de Shell que se incluirá en el objeto de datos. Recuerde que [CF \_ HDROP](clipboard.md) ya es un formato de Portapapeles válido y no es necesario registrarlo.
2.  Para cada formato que se va a transferir, coloque los datos asociados en un objeto de memoria global o cree un objeto que proporcione acceso a los datos a través de una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . Las interfaces **IStream** y **IStorage** se crean mediante técnicas com estándar. Para obtener información sobre cómo controlar los objetos de memoria global, vea [Cómo agregar un objeto de memoria global a un objeto de datos](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Cree estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) para cada formato.
4.  Cree una instancia de un objeto de datos.
5.  Cargue los datos en el objeto de datos llamando al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cada formato admitido y pasando las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) del formato.
6.  Con las transferencias de datos del portapapeles, llame a [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) para colocar un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos en el portapapeles. Para las transferencias de arrastrar y colocar, inicie un *bucle de arrastre* llamando a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop). El puntero **IDataObject** se pasará al destino de colocación cuando se quiten los datos, finalizando el bucle de arrastre.

El objeto de datos ya está listo para transferirse al destino. Para las transferencias de datos del portapapeles, el objeto simplemente se mantiene hasta que el destino lo solicita llamando a [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). En el caso de las transferencias de datos de arrastrar y colocar, el objeto de datos es responsable de crear un icono para representar los datos y moverlos a medida que el usuario mueve el cursor. Mientras el objeto está en el bucle de arrastre, el origen recibe información de estado a través de su interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Para obtener más información, consulte [implementación de IDropSource](#implementing-idropsource).

El origen no recibe ninguna notificación si un destino recupera el objeto de datos del portapapeles. Cuando un objeto se coloca en un destino mediante una operación de arrastrar y colocar, se devolverá la función [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) a la que se llamó para iniciar el bucle de arrastre.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Cómo agregar un objeto de memoria global a un objeto de datos

Muchos de los formatos de datos de Shell tienen el formato de un objeto de memoria global. Utilice el procedimiento siguiente para crear un formato que contenga un objeto de memoria global y cargarlo en el objeto de datos:

1.  Cree una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Establezca el miembro **cfFormat** en el valor de formato del portapapeles adecuado y el miembro **tymed** en tymed \_ HGLOBAL.
2.  Cree una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . Establezca el miembro **tymed** en tymed \_ HGLOBAL.
3.  Cree un objeto de memoria global llamando a [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) para asignar un bloque de memoria de tamaño adecuado.
4.  Asigne el bloque de datos que se transferirá a la dirección devuelta por [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc).
5.  Asigne la dirección del objeto de memoria global al miembro **hGlobal** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .
6.  Cargue el formato en el objeto de datos llamando a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) y pasando las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) creadas en los pasos anteriores.

La siguiente función de ejemplo crea un objeto de memoria global que contiene un valor **DWORD** y lo carga en un objeto de datos. El parámetro **pdtobj** es un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos, **CF** es el valor de formato del portapapeles y **DW** es el valor de los datos.


```C++
STDAPI DataObj_SetDWORD(IDataObject *pdtobj, UINT cf, DWORD dw)
{
    FORMATETC fmte = {(CLIPFORMAT) cf, 
                      NULL, 
                      DVASPECT_CONTENT, 
                      -1, 
                      TYMED_HGLOBAL};
    STGMEDIUM medium;

    HRESULT hres = E_OUTOFMEMORY;
    DWORD *pdw = (DWORD *)GlobalAlloc(GPTR, sizeof(DWORD));
    
    if (pdw)
    {
        *pdw = dw;       
        medium.tymed = TYMED_HGLOBAL;
        medium.hGlobal = pdw;
        medium.pUnkForRelease = NULL;

        hres = pdtobj->SetData(&fmte, &medium, TRUE);
 
        if (FAILED(hres))
            GlobalFree((HGLOBAL)pdw);
    }
    return hres;
}
```



### <a name="implementing-idataobject"></a>Implementar IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) es la interfaz principal de un objeto de datos. Debe ser implementada por todos los objetos de datos. Lo usan tanto el origen como el destino para una variedad de propósitos, entre los que se incluyen:

-   Cargar datos en el objeto de datos.
-   Extraer datos del objeto de datos.
-   Determinar qué tipos de datos se encuentran en el objeto de datos.
-   Proporcionar comentarios al objeto de datos en el resultado de la transferencia de datos.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) es compatible con una serie de métodos. En esta sección se describe cómo implementar los tres métodos más importantes para los objetos de datos de Shell, [SetData](#setdata-method), [del EnumFormatEtc](#enumformatetc-method)y [GetData](#getdata-method). Para obtener una explicación de los otros métodos, vea la referencia de **IDataObject** .

### <a name="setdata-method"></a>SetData (método)

La función principal del método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) es permitir al origen cargar datos en el objeto de datos. Para cada formato que se va a incluir, el origen crea una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para identificar el formato y una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) para contener un puntero a los datos. Después, el origen llama al método **IDataObject:: SetData** del objeto y pasa las estructuras **FORMATETC** y **STGMEDIUM** del formato. El método debe almacenar esta información para que esté disponible cuando el destino llame a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extraer datos del objeto.

Sin embargo, al transferir archivos, el shell suele colocar la información de cada archivo que se va a transferir a un formato [CFSTR \_ FILECONTENTS](clipboard.md) independiente. Para distinguir los distintos archivos, el miembro **lIndex** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) de cada archivo se establece en un valor de índice que identifica el archivo determinado. La implementación de [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) debe ser capaz de almacenar varios \_ formatos de CFSTR FILECONTENTS que solo difieren en los miembros de **lIndex** .

Mientras el cursor está sobre la ventana de destino, el destino puede usar el [objeto auxiliar de arrastrar y colocar](#using-the-drag-and-drop-helper-object) para especificar la imagen de arrastre. El objeto auxiliar de arrastrar y colocar llama a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cargar formatos privados en el objeto de datos que se usan para la compatibilidad entre procesos. Para admitir el objeto auxiliar de arrastrar y colocar, la implementación de **IDataObject:: SetData** debe ser capaz de aceptar y almacenar formatos privados arbitrarios.

Una vez que se han quitado los datos, algunos tipos de transferencia de datos de Shell requieren que el destino llame a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para proporcionar al objeto de datos información sobre el resultado de la operación de colocar. Por ejemplo, al mover archivos con una operación de movimiento optimizada, el destino normalmente elimina los archivos originales, pero no es necesario hacerlo. El destino informa al objeto de datos de si eliminó los archivos mediante una llamada a **IDataObject:: SetData** con un formato [CFSTR \_ LOGICALPERFORMEDDROPEFFECT](clipboard.md) . Hay otros formatos del [portapapeles de Shell](clipboard.md) que también usa el destino para pasar información al objeto de datos. La implementación de **IDataObject:: SetData** debe ser capaz de reconocer estos formatos y responder de forma adecuada. Para más información, consulte [Administración de escenarios de transferencia de datos de Shell](datascenarios.md).

### <a name="enumformatetc-method"></a>Método del EnumFormatEtc

Cuando el destino recibe un objeto de datos, normalmente llama a [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para determinar qué formatos contiene el objeto. El método crea un objeto de enumeración OLE y devuelve un puntero a la interfaz [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) del objeto. A continuación, el destino utiliza la interfaz para enumerar los formatos disponibles.

Un objeto de enumeración siempre debe enumerar los formatos disponibles en orden de calidad, empezando por el mejor. La calidad relativa de los formatos se define mediante el origen de la colocación. En general, los formatos de mayor calidad contienen los datos más completos y completos. Por ejemplo, una imagen de color de 24 bits normalmente se consideraría de mayor calidad que una versión de escala de grises de esa imagen. La razón para enumerar formatos en orden de calidad es que los destinos normalmente se enumeran hasta que llegan a un formato que admiten y, a continuación, usan ese formato para extraer los datos. Para que este procedimiento produzca el mejor formato disponible que pueda admitir el destino, los formatos se deben enumerar en orden de calidad.

Un objeto de enumeración para los datos de Shell se implementa prácticamente de la misma manera que para otros tipos de transferencia de datos, con una excepción importante. Dado que los objetos de datos normalmente contienen un solo elemento de datos por formato, normalmente enumeran todos los formatos que se pasan a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Sin embargo, como se describe en la sección del [método SetData](#setdata-method) , los objetos de datos de Shell pueden contener varios formatos de [CFSTR \_ FILECONTENTS](clipboard.md) .

Dado que el propósito de [**IDataObject:: del EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) es permitir que el destino determine qué tipos de datos están presentes, no es necesario enumerar más de un formato de [CFSTR \_ FILECONTENTS](clipboard.md) . Si el destino necesita saber cuántos de estos formatos contiene el objeto de datos, el destino puede recuperar esa información del formato de CFSTR FILEDESCRIPTOR que lo acompaña \_ . Para obtener más información sobre cómo implementar **IDataObject:: del EnumFormatEtc**, consulte la documentación de referencia del método.

### <a name="getdata-method"></a>Método GetData

El destino llama a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extraer un formato de datos determinado. El destino especifica el formato pasando la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) adecuada. **IDataObject:: GetData** devuelve la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) del formato.

El destino puede establecer el miembro **tymed** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en un valor XXX de tymed específico \_  para especificar qué mecanismo de transferencia de datos usará para extraer los datos. Sin embargo, el destino también puede hacer una solicitud más genérica y dejar que el objeto de datos decida. Para solicitar al objeto de datos que seleccione el mecanismo de transferencia de datos, el destino establece todos los valores de TYMED \_ *XXX* que admite. [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) selecciona uno de estos mecanismos de transferencia de datos y devuelve la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) adecuada. Por ejemplo, **tymed** se establece normalmente en tymed \_ HGLOBAL \| tymed \_ ISTREAM \| tymed \_ ISTORAGE para solicitar cualquiera de los tres mecanismos de transferencia de datos de Shell.

> [!Note]  
> Dado que puede haber varios formatos de [CFSTR \_ FILECONTENTS](clipboard.md) , los miembros **cfFormat** y **tymed** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) no son suficientes para indicar qué estructura de [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) debe devolver [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) . En el \_ formato CFSTR FILECONTENTS, **IDataObject:: GetData** también debe examinar el miembro **LIndex** de la estructura **FORMATETC** para devolver la estructura **STGMEDIUM** correcta.

 

El formato de [CFSTR \_ INDRAGLOOP](clipboard.md) se coloca en los objetos de datos para permitir que los destinos comprueben el estado del bucle de arrastrar y colocar, a la vez que se evita la representación intensiva de memoria de los datos del objeto. Los datos del formato son un valor **DWORD** que se establece en un valor distinto de cero si el objeto de datos está dentro de un bucle de arrastre. El valor de los datos del formato se establece en cero si se han quitado los datos. Si un destino solicita este formato y no lo ha cargado el origen, [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) debe responder como si el origen hubiera cargado el formato con un valor de cero.

Mientras el cursor está sobre la ventana de destino, el destino puede usar el [objeto auxiliar de arrastrar y colocar](#using-the-drag-and-drop-helper-object) para especificar la imagen de arrastre. El objeto auxiliar de arrastrar y colocar llama a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cargar formatos privados en el objeto de datos que se usan para la compatibilidad entre procesos. Más adelante llama a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para recuperarlos. Para admitir el objeto auxiliar de arrastrar y colocar, la implementación del objeto de datos de Shell debe ser capaz de devolver formatos privados arbitrarios cuando se soliciten.

### <a name="implementing-idropsource"></a>Implementación de IDropSource

El origen debe crear un objeto que exponga una interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Esta interfaz permite al origen actualizar la *imagen de arrastre* que indica la posición actual del cursor y proporcionar comentarios al sistema sobre cómo finalizar una operación de arrastrar y colocar. **IDropSource** tiene dos métodos: [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) y [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback (método)

Mientras se encuentra en el bucle de arrastre, un origen de colocación es responsable de realizar un seguimiento de la posición del cursor y mostrar una imagen de arrastre adecuada. Sin embargo, en algunos casos es posible que desee cambiar la apariencia de la imagen de arrastre cuando está sobre la ventana del destino de colocación.

Cuando el cursor entra o sale de la ventana de destino y mientras se mueve sobre la ventana de destino, el sistema llama periódicamente a la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del destino. El destino responde con un valor [**DROPEFFECT**](../com/dropeffect-constants.md) que se reenvía al origen a través del método [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . Si es necesario, el origen puede modificar la apariencia del cursor según el valor de **DROPEFFECT** . Para obtener más información, consulte las referencias **GiveFeedback** y [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

### <a name="querycontinuedrag-method"></a>QueryContinueDrag (método)

Se llama a este método si el botón del mouse o el estado del teclado cambian mientras el objeto de datos está en el bucle de arrastre. Notifica al origen si se ha presionado la tecla ESC y proporciona el estado actual de las teclas modificadoras del teclado, como CTRL o Mayús. El valor devuelto del método [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) especifica una de estas tres acciones:

-   es \_ correcto. Continuar con la operación de arrastrar
-   \_Drop S \_ . Quite los datos. Después, el sistema llama al método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) del destino.
-   DRAGDROP \_ S \_ Cancelar. Finaliza el bucle de arrastre sin quitar los datos. Normalmente, este valor se devuelve si se presionó la tecla ESCAPE.

Para obtener más información, consulte las referencias [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) y [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

## <a name="how-a-target-handles-a-data-object"></a>Cómo controla un destino un objeto de datos

El destino recibe un objeto de datos cuando recupera el objeto de datos del portapapeles o lo coloca en la ventana de destino del usuario. A continuación, el destino puede extraer datos del objeto de datos. Si es necesario, el destino también puede notificar al objeto de datos el resultado de la operación. Antes de una transferencia de datos de Shell, un destino de colocación se debe preparar para la operación:

1.  El destino debe llamar a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obtener un valor de formato del portapapeles válido para todos los formatos de Shell, excepto [CF \_ HDROP](clipboard.md), que podrían estar incluidos en el objeto de datos. CF \_ HDROP ya es un formato de Portapapeles válido y no es necesario registrarlo.
2.  Para admitir una operación de arrastrar y colocar, el destino debe implementar una interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y registrar una ventana de destino. Para registrar una ventana de destino, el destino llama a [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) y pasa el identificador de la ventana y el puntero de interfaz **IDropTarget** .

En las transferencias del portapapeles, el destino no recibe ninguna notificación de que se haya colocado un objeto de datos en el portapapeles. Normalmente, una aplicación recibe una notificación de que un objeto está en el portapapeles mediante una acción del usuario, como hacer clic en el botón pegar de la barra de herramientas de la aplicación. A continuación, el destino recupera el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos del portapapeles mediante una llamada a [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). En el caso de las transferencias de datos de arrastrar y colocar, el sistema utiliza la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del destino para proporcionar al destino información sobre el progreso de la transferencia de datos:

-   El sistema llama a [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) cuando el cursor entra en la ventana de destino.
-   El sistema llama periódicamente a [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) cuando el cursor pasa sobre la ventana de destino, para dar al destino la posición actual del cursor.
-   El sistema llama a [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) cuando el cursor sale de la ventana de destino.
-   El sistema llama a [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) cuando el usuario coloca el objeto de datos en la ventana de destino.

Para obtener información sobre cómo implementar estos métodos, vea [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Cuando se quitan los datos, [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) proporciona el destino con un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos. A continuación, el destino usa esta interfaz para extraer datos del objeto de datos.

### <a name="extracting-shell-data-from-a-data-object"></a>Extraer datos de Shell de un objeto de datos

Una vez que se ha quitado o recuperado un objeto de datos del portapapeles, el destino puede extraer los datos que necesita. Normalmente, el primer paso del proceso de extracción es enumerar los formatos contenidos en el objeto de datos:

-   Llame a [**IDataObject:: del EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc). El objeto de datos crea un objeto de enumeración OLE estándar y devuelve un puntero a su interfaz [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) .
-   Use los métodos [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) para enumerar los formatos contenidos en el objeto de datos. Esta operación normalmente recupera una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para cada formato que contiene el objeto. Sin embargo, el objeto de enumeración devuelve normalmente solo una única estructura **FORMATETC** para el formato [CFSTR \_ FILECONTENTS](clipboard.md) , independientemente de cuántos formatos estén contenidos en el objeto de datos.
-   Seleccione uno o varios formatos que se extraerán y almacene sus estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) .

Para recuperar un formato determinado, pase la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) asociada a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Este método devuelve una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que proporciona acceso a los datos. Para especificar un mecanismo de transferencia de datos determinado, establezca el valor de **tymed** de la estructura **FORMATETC** en el valor de tymed \_ *XXX* correspondiente. Para solicitar al objeto de datos que seleccione un mecanismo de transferencia de datos, el destino establece los \_ valores de TYMED *XXX* para cada mecanismo de transferencia de datos que pueda controlar el destino. El objeto de datos selecciona uno de estos mecanismos de transferencia de datos y devuelve la estructura **STGMEDIUM** adecuada.

Para la mayoría de los formatos, el destino puede recuperar los datos pasando la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) que recibió al enumerar los formatos disponibles. Una excepción a esta regla es [CFSTR \_ FILECONTENTS](clipboard.md). Dado que un objeto de datos puede contener varias instancias de este formato, es posible que la estructura **FORMATETC** devuelta por el enumerador no se corresponda con el formato determinado que se desea extraer. Además de especificar los miembros **cfFormat** y **tymed** , también debe establecer el miembro **lIndex** en el valor de índice del archivo. Para obtener más información, consulte la sección *uso del \_ formato CFSTR FILECONTENTS para extraer datos de un archivo* de [administración de escenarios de transferencia de datos de Shell](datascenarios.md) .

El proceso de extracción de datos depende del tipo de puntero que contiene la estructura de [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) devuelta. Si la estructura contiene un puntero a una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) , utilice los métodos de interfaz para extraer los datos. El proceso de extracción de datos de un objeto de memoria global se describe en la sección siguiente.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Extraer un objeto de memoria global de un objeto de datos

Muchos de los formatos de datos de Shell tienen el formato de un objeto de memoria global. Utilice el siguiente procedimiento para extraer un formato que contenga un objeto de memoria global de un objeto de datos y asignar sus datos a una variable local:

1.  Cree una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Establezca el miembro **cfFormat** en el valor de formato del portapapeles adecuado y el miembro **tymed** en tymed \_ HGLOBAL.
2.  Cree una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) vacía.
3.  Llame a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)y pase punteros a las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .

    Cuando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) devuelve, la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) contendrá un puntero al objeto de memoria global que contiene los datos.

4.  Asigne los datos a una variable local llamando a [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) y pasando el miembro **hGlobal** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .
5.  Llame a [**GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) para liberar el bloqueo en el objeto de memoria global.
6.  Llame a [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) para liberar el objeto de memoria global.

> [!Note]  
> Debe usar [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) para liberar el objeto de memoria global, no [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree).

 

En el ejemplo siguiente se muestra cómo extraer un valor **DWORD** almacenado como un objeto de memoria global de un objeto de datos. El parámetro **pdtobj** es un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos, **CF** es el formato del portapapeles que identifica los datos deseados y **pdwOut** se usa para devolver el valor de los datos.


```C++
STDAPI DataObj_GetDWORD(IDataObject *pdtobj, UINT cf, DWORD *pdwOut)
{    STGMEDIUM medium;
   FORMATETC fmte = {(CLIPFORMAT) cf, NULL, DVASPECT_CONTENT, -1, 
       TYMED_HGLOBAL};
    HRESULT hres = pdtobj->GetData(&fmte, &medium);
    if (SUCCEEDED(hres))
   {
       DWORD *pdw = (DWORD *)GlobalLock(medium.hGlobal);
       if (pdw)
       {
           *pdwOut = *pdw;
           GlobalUnlock(medium.hGlobal);
       }
       else
       {
           hres = E_UNEXPECTED;
       }
       ReleaseStgMedium(&medium);
   }
   return hres;
}
```



### <a name="implementing-idroptarget"></a>Implementar IDropTarget

El sistema utiliza la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para comunicarse con el destino mientras el cursor está sobre la ventana de destino. Las respuestas del destino se reenvían al origen a través de su interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Dependiendo de la respuesta, el origen puede modificar el icono que representa los datos. Si el destino de colocación debe especificar el icono de datos, puede hacerlo mediante la creación de un [objeto auxiliar de arrastrar y colocar](#using-the-drag-and-drop-helper-object).

Con las operaciones convencionales de arrastrar y colocar, el destino informa al objeto de datos del resultado de la operación estableciendo el parámetro *pdwEffect* de [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) en el valor de [**DROPEFFECT**](../com/dropeffect-constants.md) adecuado. Con los objetos de datos de Shell, es posible que el destino también tenga que llamar a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Para obtener una explicación de cómo los destinos deben responder para distintos escenarios de transferencia de datos, vea [administrar escenarios de transferencia de datos de Shell](datascenarios.md).

En las secciones siguientes se explica brevemente cómo implementar los métodos [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)y [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) . Para obtener más información, consulte la documentación de referencia.

### <a name="dragenter-method"></a>DragEnter (método)

El sistema llama al método [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) cuando el cursor entra en la ventana de destino. Sus parámetros proporcionan el destino con la ubicación del cursor, el estado de las teclas modificadoras del teclado, como la tecla CTRL, y un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos. El destino es responsable del uso de esa interfaz para determinar si puede aceptar cualquiera de los formatos contenidos en el objeto de datos. Si es posible, normalmente deja el valor de *pdwEffect* sin modificar. Si no puede aceptar datos del objeto de datos, establece el parámetro *pdwEffect* en DROPEFFECT \_ None. El sistema pasa el valor de este parámetro a la interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) del objeto de datos para permitir que muestre la imagen de arrastre adecuada.

Los destinos no deben usar el método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para representar los datos de Shell antes de que se hayan quitado. La representación completa de los datos del objeto para cada instancia de este tipo puede provocar que se detenga el cursor de arrastre. Para evitar este problema, algunos objetos de Shell contienen un formato de [CFSTR \_ INDRAGLOOP](clipboard.md) . Al extraer este formato, los destinos pueden comprobar el estado del bucle de arrastre y evitar la representación de los datos del objeto con un uso intensivo de la memoria. El valor de los datos del formato es un valor **DWORD** que se establece en un valor distinto de cero si el objeto de datos está dentro de un bucle de arrastre. El valor de los datos del formato se establece en cero si se han quitado los datos.

Si el destino puede aceptar datos del objeto de datos, debe examinar **grfKeyState** para determinar si se ha presionado alguna tecla modificadora para modificar el comportamiento de eliminación normal. Por ejemplo, la operación predeterminada suele ser un movimiento, pero si se presiona la tecla CTRL se suele indicar una operación de copia.

Mientras el cursor está sobre la ventana de destino, el destino puede usar el [objeto auxiliar de arrastrar y colocar](#using-the-drag-and-drop-helper-object) para reemplazar la imagen de arrastre del objeto de datos por la suya propia. Si es así, [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) debe llamar a [**IDropTargetHelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) para pasar la información contenida en los parámetros *DragEnter* al objeto auxiliar de arrastrar y colocar.

### <a name="dragover-method"></a>DragOver (método)

Cuando el cursor se mueve dentro de la ventana de destino, el sistema llama periódicamente al método [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) . Sus parámetros proporcionan el destino con la ubicación del cursor y el estado de las teclas modificadoras del teclado, como la tecla CTRL. **IDropTarget::D ragover** tiene prácticamente las mismas responsabilidades que [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)y las implementaciones suelen ser muy similares.

Si el destino usa el objeto auxiliar de arrastrar y colocar, [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) debe llamar a [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) para reenviar la información contenida en los parámetros de *DragOver* al objeto auxiliar de arrastrar y colocar.

### <a name="drop-method"></a>Drop (método)

El sistema llama al método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) para notificar al destino que el usuario ha quitado los datos, normalmente liberando el botón del mouse. **IDropTarget::D ROP** tiene los mismos parámetros que [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). Normalmente, el destino responde mediante la extracción de uno o más formatos del objeto de datos. Cuando termine, el destino debe establecer el parámetro *pdwEffect* en un valor [**DROPEFFECT**](../com/dropeffect-constants.md) que indique el resultado de la operación. En algunos tipos de transferencia de datos de Shell, el destino también debe llamar a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para pasar un formato con información adicional sobre el resultado de la operación al objeto de datos. Para obtener una explicación detallada, vea [administrar escenarios de transferencia de datos de Shell](datascenarios.md).

Si el destino usa el objeto auxiliar de arrastrar y colocar, [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) debe llamar a [**IDropTargetHelper::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) para reenviar la información contenida en los parámetros [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) al objeto auxiliar de arrastrar y colocar.

## <a name="using-the-drag-and-drop-helper-object"></a>Usar el objeto auxiliar de arrastrar y colocar

El shell exporta el objeto auxiliar de arrastrar y colocar (CLSID \_ DragDropHelper) para permitir que los destinos especifiquen la imagen de arrastre mientras está sobre la ventana de destino. Para usar el objeto auxiliar de arrastrar y colocar, cree un objeto de servidor en proceso llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un identificador de clase (CLSID) de CLSID \_ DragDropHelper. El objeto auxiliar de arrastrar y colocar expone dos interfaces que se utilizan de la siguiente manera:

-   La interfaz [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) permite que el destino de colocación especifique un icono para representar el objeto de datos.
-   La interfaz [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permite que el destino de colocación informe al objeto auxiliar de arrastrar y colocar de la ubicación del cursor y para mostrar u ocultar el icono de los datos.

### <a name="using-the-idragsourcehelper-interface"></a>Uso de la interfaz IDragSourceHelper

La interfaz [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) se expone mediante el objeto auxiliar de arrastrar y colocar para permitir que un destino de colocación proporcione la imagen que se mostrará mientras el cursor está sobre la ventana de destino. **IDragSourceHelper** proporciona dos maneras alternativas de especificar el mapa de bits que se va a usar como imagen de arrastre:

-   Los destinos de colocación que tienen una ventana pueden registrar un \_ mensaje de ventana di GETDRAGIMAGE para él inicializando el objeto auxiliar de arrastrar y colocar con [**IDragSourceHelper:: InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Cuando el destino recibe un \_ mensaje di GETDRAGIMAGE, el controlador coloca la información de mapa de bits de la imagen de arrastre en la estructura [**SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) que se pasa como el valor *lParam* del mensaje.
-   Los destinos de colocación sin ventanas especifican un mapa de bits cuando inicializan el objeto auxiliar de arrastrar y colocar con [**IDragSourceHelper:: InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap).

### <a name="using-the-idroptargethelper-interface"></a>Usar la interfaz IDropTargetHelper

Esta interfaz permite que el destino de colocación notifique el objeto auxiliar de arrastrar y colocar cuando el cursor entra o sale del destino. Mientras el cursor está sobre la ventana de destino, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permite que el destino proporcione al objeto auxiliar de arrastrar y colocar la información que el destino recibe a través de su interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .

Cuatro de los métodos [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) ,[**IDropTargetHelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper::D Ragleave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**idroptargethelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)y [**IDropTargetHelper::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop), están asociados con el método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del mismo nombre. Para usar el objeto auxiliar de arrastrar y colocar, cada uno de los métodos **IDropTarget** debe llamar al método **IDropTargetHelper** correspondiente para reenviar la información al objeto auxiliar de arrastrar y colocar. El quinto método **IDropTargetHelper** , [**IDropTargetHelper:: show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show), notifica al objeto auxiliar de arrastrar y colocar para mostrar u ocultar la imagen de arrastre. Este método se usa al arrastrar sobre una ventana de destino en un modo de vídeo de baja profundidad de color. Permite que el destino oculte la imagen de arrastre mientras está pintando la ventana.

 

 
