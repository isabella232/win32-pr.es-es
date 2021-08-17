---
description: El objeto de datos es fundamental para todas las transferencias de datos de Shell.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Objeto de datos de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de7c05810e3f641b5216d0923fef9798773678683f7f8c8af5cb90389f794da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444045"
---
# <a name="shell-data-object"></a>Objeto de datos de shell

El objeto de datos es fundamental para todas las transferencias de datos de Shell. Es principalmente un contenedor para contener los datos transferidos. Sin embargo, el destino también puede comunicarse con el objeto de datos para facilitar algunos tipos especializados de transferencia de datos de Shell, como los movimientos optimizados. En este tema se proporciona una explicación general de cómo funcionan los objetos de datos de Shell, cómo se construyen mediante un origen y cómo se controlan mediante un destino. Para obtener una explicación detallada de cómo usar objetos de datos para transferir diferentes tipos de datos de Shell, vea [Handling Shell Data Transfer Scenarios](datascenarios.md).

-   [Cómo funcionan los objetos de datos](#how-data-objects-work)
    -   [Formatos del Portapapeles](#clipboard-formats)
    -   [Estructura FORMATETC](#formatetc-structure)
    -   [Estructura STGMEDIUM](#stgmedium-structure)
-   [Cómo un origen crea un objeto de datos](#how-a-source-creates-a-data-object)
    -   [Cómo agregar un objeto de memoria global a un objeto de datos](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementación de IDataObject](#implementing-idataobject)
    -   [Implementación de IDropSource](#implementing-idropsource)
-   [Cómo controla un destino un objeto de datos](#how-a-target-handles-a-data-object)
    -   [Extracción de datos de shell de un objeto de datos](#extracting-shell-data-from-a-data-object)
    -   [Implementación de IDropTarget](#implementing-idroptarget)
-   [Usar el objeto auxiliar de arrastrar y colocar](#using-the-drag-and-drop-helper-object)
    -   [Uso de la interfaz IDragSourceHelper](#using-the-idragsourcehelper-interface)
    -   [Uso de la interfaz IDropTargetHelper](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Cómo funcionan los objetos de datos

Los objetos de datos son objetos del Modelo de objetos componentes (COM), creados por el origen de datos para transferir datos a un destino. Normalmente llevan más de un elemento de datos. Hay dos razones para esta práctica:

-   Aunque casi cualquier tipo de datos se puede transferir con un objeto de datos, el origen normalmente no sabe qué tipo de datos puede aceptar el destino. Por ejemplo, los datos pueden ser una parte de un documento de texto con formato. Aunque es posible que el destino pueda controlar información de formato compleja, también podría aceptar solo texto ANSI. Por esta razón, los objetos de datos suelen incluir los mismos datos en varios formatos diferentes. A continuación, el destino puede extraer los datos en un formato que pueda controlar.
-   Los objetos de datos también pueden contener elementos de datos auxiliares que no son versiones de los datos de origen. Este tipo de elemento de datos normalmente proporciona información adicional sobre la operación de transferencia de datos. Por ejemplo, el Shell usa elementos de datos auxiliares para indicar si un archivo se va a copiar o mover.

### <a name="clipboard-formats"></a>Formatos del Portapapeles

Cada elemento de datos de un objeto de datos tiene un formato asociado, normalmente denominado formato *del Portapapeles*. Hay una serie de formatos estándar del Portapapeles, declarados en Winuser.h, que corresponden a tipos de datos usados habitualmente. Los formatos del Portapapeles son enteros, pero normalmente se hace referencia a ellos por su nombre equivalente, que tiene el formato CF \_ *XXX*. Por ejemplo, el formato del Portapapeles para el texto ANSI es CF \_ TEXT.

Las aplicaciones pueden ampliar el intervalo de formatos disponibles del Portapapeles mediante la definición de formatos privados. Para definir un formato privado, una aplicación llama a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) con una cadena que identifica el formato. El entero sin signo que devuelve la función es un valor de formato válido que se puede usar igual que un formato estándar del Portapapeles. Sin embargo, tanto el origen como el destino deben registrar el formato para poder usarlo. Con una excepción,[CF \_ HDROP,](clipboard.md)los formatos del Portapapeles usados para transferir datos de Shell se definen como formatos privados. Deben estar registrados por el origen y el destino para poder usarse. Para obtener una descripción de los formatos de Portapapeles de Shell disponibles, vea Formatos del Portapapeles de Shell.

Aunque hay algunas excepciones, los objetos de datos normalmente contienen solo un elemento de datos para cada formato del Portapapeles que admitan. Esta correlación uno a uno entre el formato y los datos permite que el valor de formato se utilice como identificador para el elemento de datos asociado. De hecho, al analizar el contenido de un objeto de datos, un elemento determinado de datos normalmente se denomina "formato" y se hace referencia a él por su nombre de formato. Por ejemplo, frases como "Extraer el formato CF \_ TEXT..." se usan normalmente al analizar el elemento de datos de texto ANSI de un objeto de datos.

Cuando el destino de colocación recibe el puntero al objeto de datos, el destino de colocación enumera los formatos disponibles para determinar qué tipos de datos están disponibles. A continuación, solicita uno o varios de los formatos disponibles y extrae los datos. La forma específica en que el destino extrae datos de Shell de un objeto de datos varía según el formato; esto se describe en detalle en [How a Target Handles a Data Object](#how-a-target-handles-a-data-object).

Con transferencias de datos sencillas del Portapapeles, los datos se colocan en un objeto de memoria global. La dirección de ese objeto se coloca en el Portapapeles, junto con su formato. El formato del Portapapeles indica al destino qué tipo de datos encontrará en la dirección asociada. Aunque las transferencias sencillas del Portapapeles son fáciles de implementar:

-   Los objetos de datos proporcionan una manera mucho más flexible de transferir datos.
-   Los objetos de datos son más adecuados para transferir grandes cantidades de datos.
-   Los objetos de datos se deben usar para transferir datos con una operación de arrastrar y colocar.

Por estos motivos, todas las transferencias de datos de Shell usan objetos de datos. Con objetos de datos, los formatos del Portapapeles no se usan directamente. En su lugar, los elementos de datos se identifican con una generalización del formato del Portapapeles, [**una estructura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc)

### <a name="formatetc-structure"></a>Estructura FORMATETC

La [**estructura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) es una versión extendida de un formato del Portapapeles. Como se usa para las transferencias de datos de Shell, la **estructura FORMATETC** tiene las siguientes características:

-   Un elemento de datos todavía se identifica por su formato de Portapapeles, en el **miembro cfFormat.**
-   La transferencia de datos no se limita a los objetos de memoria global. El **miembro tymed** se usa para indicar el mecanismo de transferencia de datos contenido en la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) asociada. Se establece en uno de los valores [**\_ XXX de TYMED.**](/windows/win32/api/objidl/ne-objidl-tymed)
-   El shell usa el **miembro lIndex** con su formato [ \_ FILECONTENTS de CFSTR](clipboard.md) para permitir que un objeto de datos contenga más de un elemento de datos por formato. Para obtener una explicación sobre cómo usar este formato, vea la sección Using *the CFSTR \_ FILECONTENTS Format to Extract Data from a File* de Handling Shell Data Transfer [Scenarios](datascenarios.md).
-   El **miembro dwAspect** normalmente se establece en DVASPECT \_ CONTENT. Sin embargo, hay tres valores definidos en Shlobj.h que se pueden usar para la transferencia de datos de Shell. 

    | Value               | Descripción                                                                                       |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | DVASPECT \_ COPY      | Se usa para indicar que el formato representa una copia de los datos.                                   |
    | VÍNCULO \_ DVASPECT      | Se usa para indicar que el formato representa un acceso directo a los datos.                               |
    | DVASPECT \_ SHORTNAME | Se usa con el formato CF HDROP para solicitar una ruta de \_ acceso de archivo con los nombres abreviados al formato 8.3. |

    

     

-   El **miembro ptd** no se usa para las transferencias de datos de Shell y normalmente se establece en **NULL.**

### <a name="stgmedium-structure"></a>Estructura STGMEDIUM

La [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) proporciona acceso a los datos que se transfieren. Se admiten tres mecanismos de transferencia de datos para los datos de Shell:

-   Objeto de memoria global.
-   Interfaz [**IStream.**](/windows/win32/api/objidl/nn-objidl-istream)
-   Interfaz [**IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage)

El **miembro tymed** de la [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) es un valor [**\_ XXX de TYMED**](/windows/win32/api/objidl/ne-objidl-tymed) que identifica el mecanismo de transferencia de datos. El segundo miembro es un puntero que usa el destino para extraer los datos. El puntero puede ser uno de varios tipos, dependiendo del **valor tymed.** Los tres **valores de tymed** que se usan para las transferencias de datos de Shell se resumen en la tabla siguiente, junto con su nombre de miembro **STGMEDIUM** correspondiente.



| Valor de tymed     | Nombre del miembro | Descripción                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **hGlobal** | Puntero a un objeto de memoria global. Este tipo de puntero se usa normalmente para transferir pequeñas cantidades de datos. Por ejemplo, el Shell usa objetos de memoria global para transferir cadenas de texto cortas, como nombres de archivo o direcciones URL.                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | Puntero a una [**interfaz IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Este tipo de puntero es el preferido para la mayoría de las transferencias de datos de Shell porque requiere relativamente poca memoria en comparación con TYMED \_ HGLOBAL. Además, el mecanismo de transferencia de datos ISTREAM de TYMED no requiere que el origen almacene \_ sus datos de ninguna manera determinada. |
| TYMED \_ ISTORAGE | **Pstg**    | Puntero a una [**interfaz IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) El destino llama a los métodos de interfaz para extraer los datos. Al igual que TYMED \_ ISTREAM, este tipo de puntero requiere relativamente poca memoria. Sin embargo, dado que TYMED ISTORAGE es menos flexible que \_ TYMED ISTREAM, no se \_ usa con frecuencia.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Cómo crea un origen un objeto de datos

Cuando un usuario inicia una transferencia de datos de Shell, el origen es responsable de crear un objeto de datos y cargarlo con datos. En el procedimiento siguiente se resume el proceso:

1.  Llame [a RegisterClipboardFormat para](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) obtener un valor de formato de Portapapeles válido para cada formato de Shell que se incluirá en el objeto de datos. Recuerde que [CF \_ HDROP](clipboard.md) ya es un formato válido del Portapapeles y no es necesario registrarlo.
2.  Para cada formato que se va a transferir, coloque los datos asociados en un objeto de memoria global o cree un objeto que proporciona acceso a los datos a través de una [**interfaz IStream**](/windows/win32/api/objidl/nn-objidl-istream) [**o IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) Las **interfaces IStream** **e IStorage** se crean mediante técnicas COM estándar. Para obtener una explicación sobre cómo controlar objetos de memoria global, vea Cómo agregar un objeto de [memoria global a un objeto de datos](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Cree [**estructuras FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) [**y STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) para cada formato.
4.  Cree una instancia de un objeto de datos.
5.  Cargue los datos en el objeto de datos llamando al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cada formato admitido y pasando las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM del**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) formato.
6.  Con las transferencias de datos del Portapapeles, llame a [**OleSetClipboard para**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) colocar un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos en el Portapapeles. Para las transferencias de arrastrar y colocar, inicie un *bucle de arrastre* mediante una llamada a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop). El **puntero IDataObject** se pasará al destino de colocación cuando se coloquen los datos, finalizando el bucle de arrastre.

El objeto de datos ya está listo para transferirse al destino. Para las transferencias de datos del Portapapeles, el objeto simplemente se mantiene hasta que el destino lo solicita mediante una [**llamada a OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Para las transferencias de datos de arrastrar y colocar, el objeto de datos es responsable de crear un icono para representar los datos y moverlos a medida que el usuario mueve el cursor. Mientras el objeto está en el bucle de arrastre, el origen recibe información de estado a través de su [**interfaz IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Para obtener más información, [vea Implementación de IDropSource.](#implementing-idropsource)

El origen no recibe ninguna notificación si un destino recupera el objeto de datos del Portapapeles. Cuando un objeto se coloca en un destino mediante una operación de arrastrar y colocar, se devolverá la función [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) a la que se llamó para iniciar el bucle de arrastre.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Cómo agregar un objeto de memoria global a un objeto de datos

Muchos de los formatos de datos de Shell tienen el formato de un objeto de memoria global. Use el procedimiento siguiente para crear un formato que contenga un objeto de memoria global y cargarlo en el objeto de datos:

1.  Cree una [**estructura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) Establezca el **miembro cfFormat** en el valor de formato del Portapapeles adecuado y el miembro **tymed** en TYMED \_ HGLOBAL.
2.  Cree una [**estructura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Establezca el **miembro tymed** en TYMED \_ HGLOBAL.
3.  Cree un objeto de memoria global mediante una llamada a [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) para asignar un bloque de memoria de tamaño adecuado.
4.  Asigne el bloque de datos que se va a transferir a la dirección devuelta [**por GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc).
5.  Asigne la dirección del objeto de memoria global al **miembro hGlobal** de la [**estructura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
6.  Cargue el formato en el objeto de datos llamando a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) y pasando las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) creadas en los pasos anteriores.

La siguiente función de ejemplo crea un objeto de memoria global que contiene un **valor DWORD** y lo carga en un objeto de datos. El **parámetro pdtobj** es un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos, **cf** es el valor de formato del Portapapeles y **dw** es el valor de datos.


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



### <a name="implementing-idataobject"></a>Implementación de IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) es la interfaz principal de un objeto de datos. Todos los objetos de datos deben implementarlo. Tanto el origen como el destino lo usan para diversos propósitos, entre los que se incluyen:

-   Carga de datos en el objeto de datos.
-   Extraer datos del objeto de datos.
-   Determinar qué tipos de datos están en el objeto de datos.
-   Proporcionar comentarios al objeto de datos sobre el resultado de la transferencia de datos.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) admite varios métodos. En esta sección se describe cómo implementar los tres métodos más importantes para los objetos de datos de Shell, [SetData,](#setdata-method) [EnumFormatEtc](#enumformatetc-method)y [GetData.](#getdata-method) Para obtener una explicación de los otros métodos, vea la **referencia de IDataObject.**

### <a name="setdata-method"></a>SetData (método)

La función principal del [**método IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) es permitir que el origen cargue datos en el objeto de datos. Para cada formato que se va a incluir, el origen crea una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para identificar el formato y una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) para contener un puntero a los datos. A continuación, el origen llama al método **IDataObject::SetData** del objeto y pasa las estructuras **FORMATETC** y **STGMEDIUM del** formato. El método debe almacenar esta información para que esté disponible cuando el destino llame a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extraer datos del objeto .

Sin embargo, al transferir archivos, el Shell suele poner la información de cada archivo que se va a transferir a un formato [ \_ FILECONTENTS de CFSTR](clipboard.md) independiente. Para distinguir los distintos archivos, el **miembro lIndex** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) de cada archivo se establece en un valor de índice que identifica el archivo determinado. La [**implementación de IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) debe ser capaz de almacenar varios formatos FILECONTENTS de CFSTR que solo difieren \_ en sus miembros **lIndex.**

Mientras el cursor está sobre la ventana de destino, el destino puede usar el objeto auxiliar de arrastrar y colocar [para](#using-the-drag-and-drop-helper-object) especificar la imagen de arrastre. El objeto auxiliar de arrastrar y colocar llama a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cargar formatos privados en el objeto de datos que se usan para la compatibilidad entre procesos. Para admitir el objeto auxiliar de arrastrar y colocar, la implementación de **IDataObject::SetData** debe ser capaz de aceptar y almacenar formatos privados arbitrarios.

Después de quitar los datos, algunos tipos de transferencia de datos de Shell requieren que el destino llame a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para proporcionar al objeto de datos información sobre el resultado de la operación de colocación. Por ejemplo, al mover archivos con una operación de movimiento optimizada, el destino normalmente elimina los archivos originales, pero no es necesario hacerlo. El destino informa al objeto de datos si eliminó los archivos mediante una llamada a **IDataObject::SetData** con un formato [ \_ CFSTR LOGICALPERFORMEDDROPEFFECT.](clipboard.md) Hay otros formatos del [Portapapeles de Shell](clipboard.md) que también usa el destino para pasar información al objeto de datos. La **implementación de IDataObject::SetData** debe ser capaz de reconocer estos formatos y responder correctamente. Para obtener más información, vea [Handling Shell Data Transfer Scenarios](datascenarios.md).

### <a name="enumformatetc-method"></a>Método EnumFormatEtc

Cuando el destino recibe un objeto de datos, normalmente llama a [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para determinar qué formatos contiene el objeto. El método crea un objeto de enumeración OLE y devuelve un puntero a la interfaz [**IEnumFORMATETC del**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) objeto. A continuación, el destino usa la interfaz para enumerar los formatos disponibles.

Un objeto de enumeración siempre debe enumerar los formatos disponibles en orden de calidad, empezando por el mejor. La calidad relativa de los formatos se define mediante el origen de colocación. En general, los formatos de mayor calidad contienen los datos más completos y enriquecidos. Por ejemplo, una imagen de color de 24 bits normalmente se consideraría de mayor calidad que una versión de escala de grises de esa imagen. La razón para enumerar los formatos por orden de calidad es que los destinos suelen enumerarse hasta llegar a un formato que admiten y, a continuación, usan ese formato para extraer los datos. Para que este procedimiento produzca el mejor formato disponible que el destino pueda admitir, los formatos deben enumerarse en orden de calidad.

Un objeto de enumeración para los datos de Shell se implementa de la misma manera que para otros tipos de transferencia de datos, con una excepción importante. Dado que los objetos de datos normalmente contienen solo un elemento de datos por formato, normalmente enumeran todos los formatos que se pasan a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Sin embargo, como se describe en la [sección Método SetData,](#setdata-method) los objetos de datos de Shell pueden contener varios [ \_ formatos FILECONTENTS de CFSTR.](clipboard.md)

Dado que el propósito de [**IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) es permitir que el destino determine qué tipos de datos están presentes, no es necesario enumerar más de un formato [ \_ FILECONTENTS de CFSTR.](clipboard.md) Si el destino necesita saber cuántos de estos formatos contiene el objeto de datos, el destino puede recuperar esa información del formato FILEDESCRIPTOR de CFSTR \_ que lo acompaña. Para obtener más información sobre cómo implementar **IDataObject::EnumFormatEtc,** vea la documentación de referencia del método.

### <a name="getdata-method"></a>Método GetData

El destino llama [**a IDataObject::GetData para**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) extraer un formato de datos determinado. El destino especifica el formato pasando la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) adecuada. **IDataObject::GetData** devuelve la estructura [**STGMEDIUM del**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) formato.

El destino puede establecer el miembro **tymed** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en un valor XXX de TYMED específico para especificar qué mecanismo de transferencia de datos usará para \_  extraer los datos. Sin embargo, el destino también puede realizar una solicitud más genérica y dejar que el objeto de datos decida. Para pedir al objeto de datos que seleccione el mecanismo de transferencia de datos, el destino establece todos los valores XXX de TYMED \_  que admite. [**IDataObject::GetData selecciona**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) uno de estos mecanismos de transferencia de datos y devuelve la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) adecuada. Por ejemplo, **tymed** se establece normalmente en \_ \| TYMED TGLOBAL TYMED \_ \| ISTREAM TYMED ISTORAGE para solicitar cualquiera de los tres mecanismos de transferencia de datos \_ de Shell.

> [!Note]  
> Dado que puede haber varios [ \_ formatos FILECONTENTS de CFSTR,](clipboard.md) los miembros **cfFormat** y **tymed** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) no son suficientes para indicar qué estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) debe devolver. Para el formato \_ FILECONTENTS de CFSTR, **IDataObject::GetData** también debe examinar el miembro **lIndex** de la estructura **FORMATETC** para devolver la estructura **STGMEDIUM** correcta.

 

El [formato CFSTR \_ INDRAGLOOP](clipboard.md) se coloca en objetos de datos para permitir que los destinos comprueben el estado del bucle de arrastrar y colocar, al tiempo que se evita la representación intensiva de memoria de los datos del objeto. Los datos del formato son un **valor DWORD** que se establece en un valor distinto de cero si el objeto de datos está dentro de un bucle de arrastre. El valor de datos del formato se establece en cero si se han eliminado los datos. Si un destino solicita este formato y el origen no lo ha cargado, [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) debe responder como si el origen hubiera cargado el formato con un valor de cero.

Mientras el cursor está sobre la ventana de destino, el destino puede usar el objeto auxiliar de arrastrar y colocar [para](#using-the-drag-and-drop-helper-object) especificar la imagen de arrastre. El objeto auxiliar de arrastrar y colocar llama a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cargar formatos privados en el objeto de datos que se usan para la compatibilidad entre procesos. Más adelante llama [**a IDataObject::GetData para**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) recuperarlos. Para admitir el objeto auxiliar de arrastrar y colocar, la implementación del objeto de datos de Shell debe ser capaz de devolver formatos privados arbitrarios cuando se solicitan.

### <a name="implementing-idropsource"></a>Implementación de IDropSource

El origen debe crear un objeto que exponga una [**interfaz IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Esta interfaz permite al  origen actualizar la imagen de arrastre que indica la posición actual del cursor y proporcionar comentarios al sistema sobre cómo finalizar una operación de arrastrar y colocar. **IDropSource** tiene dos métodos: [**GiveFeedback y**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback (método)

Mientras se encuentra en el bucle de arrastre, un origen de colocación es responsable de realizar un seguimiento de la posición del cursor y mostrar una imagen de arrastre adecuada. Sin embargo, en algunos casos es posible que quiera cambiar la apariencia de la imagen de arrastre cuando se encuentra sobre la ventana del destino de colocación.

Cuando el cursor entra o sale de la ventana de destino y se mueve sobre la ventana de destino, el sistema llama periódicamente a la interfaz [**IDropTarget del**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) destino. El destino responde con un [**valor DROPEFFECT**](../com/dropeffect-constants.md) que se reenvía al origen mediante el [**método GiveFeedback.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) Si procede, el origen puede modificar la apariencia del cursor en función del **valor DROPEFFECT.** Para más información, consulte las **referencias GiveFeedback** y [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

### <a name="querycontinuedrag-method"></a>QueryContinueDrag (método)

Se llama a este método si el estado del teclado o el botón del mouse cambia mientras el objeto de datos está en el bucle de arrastre. Notifica al origen si se ha presionado la tecla ESC y proporciona el estado actual de las teclas modificadoras de teclado, como CTRL o MAYÚS. El valor devuelto [**del método QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) especifica una de estas tres acciones:

-   S \_ OK. Continuar con la operación de arrastre
-   ARRASTRARDROP \_ S \_ DROP. Quitar los datos. A continuación, el sistema llama al [**método IDropTarget::D rop del**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) destino.
-   DRAGDROP \_ S \_ CANCEL. Finalice el bucle de arrastre sin quitar los datos. Este valor se devuelve normalmente si se presionó la tecla ESCAPE.

Para más información, consulte las [**referencias QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) y [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

## <a name="how-a-target-handles-a-data-object"></a>Cómo controla un destino un objeto de datos

El destino recibe un objeto de datos cuando recupera el objeto de datos del Portapapeles o el usuario lo deja en la ventana de destino. A continuación, el destino puede extraer datos del objeto de datos. Si es necesario, el destino también puede notificar al objeto de datos el resultado de la operación. Antes de una transferencia de datos de Shell, un destino de colocación debe prepararse para la operación:

1.  El destino debe llamar a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obtener un valor de formato de Portapapeles válido para todos los formatos de Shell, distintos de [CF \_ HDROP,](clipboard.md)que podrían incluirse en el objeto de datos. CF \_ HDROP ya es un formato válido del Portapapeles y no es necesario registrarlo.
2.  Para admitir una operación de arrastrar y colocar, el destino debe implementar una [**interfaz IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y registrar una ventana de destino. Para registrar una ventana de destino, el destino llama a [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) y pasa el identificador de la ventana y el puntero de interfaz **IDropTarget.**

Para las transferencias del Portapapeles, el destino no recibe ninguna notificación de que se ha colocado un objeto de datos en el Portapapeles. Normalmente, una acción del usuario notifica a una aplicación que un objeto está en el Portapapeles, como hacer clic en el botón Pegar de la barra de herramientas de la aplicación. A continuación, el destino recupera el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos del Portapapeles mediante una llamada [**a OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Para las transferencias de datos de arrastrar y colocar, el sistema usa la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del destino para proporcionar al destino información sobre el progreso de la transferencia de datos:

-   El sistema llama [**a IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) cuando el cursor entra en la ventana de destino.
-   El sistema llama periódicamente a [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) a medida que el cursor pasa por la ventana de destino para proporcionar al destino la posición actual del cursor.
-   El sistema llama [**a IDropTarget::D ragLeave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) cuando el cursor sale de la ventana de destino.
-   El sistema llama [**a IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) cuando el usuario quita el objeto de datos en la ventana de destino.

Para obtener una explicación de cómo implementar estos métodos, vea [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Cuando se descartan los datos, [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) proporciona al destino un puntero a la interfaz [**IDataObject del objeto de**](/windows/win32/api/objidl/nn-objidl-idataobject) datos. A continuación, el destino usa esta interfaz para extraer datos del objeto de datos.

### <a name="extracting-shell-data-from-a-data-object"></a>Extraer datos del shell de un objeto de datos

Una vez que se ha eliminado o recuperado un objeto de datos del Portapapeles, el destino puede extraer los datos que necesita. El primer paso del proceso de extracción suele ser enumerar los formatos contenidos en el objeto de datos:

-   Llame [**a IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc). El objeto de datos crea un objeto de enumeración OLE estándar y devuelve un puntero a su [**interfaz IEnumFORMATETC.**](/windows/win32/api/objidl/nn-objidl-ienumformatetc)
-   Use los [**métodos IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) para enumerar los formatos contenidos en el objeto de datos. Esta operación normalmente recupera una [**estructura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para cada formato que contiene el objeto. Sin embargo, el objeto de enumeración normalmente devuelve solo una única estructura **FORMATETC** para el formato [ \_ FILECONTENTS de CFSTR,](clipboard.md) independientemente de cuántos formatos de este tipo contenga el objeto de datos.
-   Seleccione uno o varios formatos que se extraerán y almacene sus estructuras [**FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc)

Para recuperar un formato determinado, pase la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) asociada a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Este método devuelve una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que proporciona acceso a los datos. Para especificar un mecanismo de transferencia de datos determinado, establezca el valor **tymed** de la estructura **FORMATETC** en el valor XXX de TYMED \_  correspondiente. Para pedir al objeto de datos que seleccione un mecanismo de transferencia de datos, el destino establece los valores XXX de TYMED para cada mecanismo de transferencia de datos que \_  el destino puede controlar. El objeto de datos selecciona uno de estos mecanismos de transferencia de datos y devuelve la estructura **STGMEDIUM** adecuada.

Para la mayoría de los formatos, el destino puede recuperar los datos pasando la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) que recibió al enumerar los formatos disponibles. Una excepción a esta regla es [CFSTR \_ FILECONTENTS.](clipboard.md) Dado que un objeto de datos puede contener varias instancias de este formato, es posible que la estructura **FORMATETC** devuelta por el enumerador no se corresponda con el formato concreto que desea extraer. Además de especificar los miembros **cfFormat** y **tymed,** también debe establecer el miembro **lIndex** en el valor de índice del archivo. Para obtener más información, vea la sección *Using the CFSTR \_ FILECONTENTS Format to Extract Data from a File* (Uso del formato FILECONTENTS de CFSTR para extraer datos de un archivo) de [Handling Shell Data Transfer Scenarios](datascenarios.md)

El proceso de extracción de datos depende del tipo de puntero contenido en la estructura [**STGMEDIUM devuelta.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Si la estructura contiene un puntero a una [**interfaz IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage,**](/windows/win32/api/objidl/nn-objidl-istorage) use los métodos de interfaz para extraer los datos. El proceso de extracción de datos de un objeto de memoria global se describe en la sección siguiente.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Extracción de un objeto de memoria global de un objeto de datos

Muchos de los formatos de datos de Shell tienen el formato de un objeto de memoria global. Use el procedimiento siguiente para extraer un formato que contiene un objeto de memoria global de un objeto de datos y asignar sus datos a una variable local:

1.  Cree una [**estructura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) Establezca el **miembro cfFormat** en el valor de formato del Portapapeles adecuado y el miembro **tymed** en TYMED \_ HGLOBAL.
2.  Cree una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) vacía.
3.  Llame [**a IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)y pase punteros a las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

    Cuando [**se devuelve IDataObject::GetData,**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) contendrá un puntero al objeto de memoria global que contiene los datos.

4.  Asigne los datos a una variable local llamando a [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) y pasando el **miembro hGlobal** de la [**estructura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
5.  Llame [**a GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) para liberar el bloqueo en el objeto de memoria global.
6.  Llame [**a ReleaseStgMedium para**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) liberar el objeto de memoria global.

> [!Note]  
> Debe usar [**ReleaseStgMedium para**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) liberar el objeto de memoria global, no [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree).

 

En el ejemplo siguiente se muestra cómo extraer un **valor DWORD** almacenado como un objeto de memoria global de un objeto de datos. El **parámetro pdtobj** es un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos, **cf** es el formato del Portapapeles que identifica los datos deseados y **pdwOut** se usa para devolver el valor de datos.


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



### <a name="implementing-idroptarget"></a>Implementación de IDropTarget

El sistema usa la [**interfaz IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para comunicarse con el destino mientras el cursor está sobre la ventana de destino. Las respuestas del destino se reenvía al origen a través de su [**interfaz IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) En función de la respuesta, el origen puede modificar el icono que representa los datos. Si el destino de colocación necesita especificar el icono de datos, puede hacerlo mediante la creación de un objeto auxiliar de arrastrar [y colocar](#using-the-drag-and-drop-helper-object).

Con las operaciones convencionales de arrastrar y colocar, el destino informa al objeto de datos del resultado de la operación estableciendo el parámetro *pdwEffect* de [**IDropTarget::D rop en**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) el valor [**DROPEFFECT**](../com/dropeffect-constants.md) adecuado. Con los objetos de datos de Shell, es posible que el destino también tenga que llamar a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Para obtener una explicación de cómo deben responder los destinos para distintos escenarios de transferencia de datos, vea [Handling Shell Data Transfer Scenarios](datascenarios.md).

En las secciones siguientes se describe brevemente cómo implementar los métodos [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)e [**IDropTarget::D rop.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) Para más información, consulte la documentación de referencia.

### <a name="dragenter-method"></a>Método DragEnter

El sistema llama al [**método IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) cuando el cursor entra en la ventana de destino. Sus parámetros proporcionan al destino la ubicación del cursor, el estado de las teclas modificadoras de teclado, como la tecla CTRL, y un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos. El destino es responsable de usar esa interfaz para determinar si puede aceptar cualquiera de los formatos contenidos en el objeto de datos. Si es posible, normalmente deja el valor *de pdwEffect* sin cambios. Si no puede aceptar ningún dato del objeto de datos, establece el *parámetro pdwEffect* en DROPEFFECT \_ NONE. El sistema pasa el valor de este parámetro a la interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) del objeto de datos para permitirle mostrar la imagen de arrastre adecuada.

Los destinos no deben usar [**el método IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para representar los datos de Shell antes de que se hayan eliminado. La representación completa de los datos del objeto para cada repetición de este tipo podría hacer que el cursor de arrastre se detendría. Para evitar este problema, algunos objetos de Shell contienen un formato [ \_ CFSTR INDRAGLOOP.](clipboard.md) Al extraer este formato, los destinos pueden comprobar el estado del bucle de arrastre y evitar la representación intensiva de memoria de los datos del objeto. El valor de datos del formato es **un DWORD** que se establece en un valor distinto de cero si el objeto de datos está dentro de un bucle de arrastre. El valor de datos del formato se establece en cero si se han eliminado los datos.

Si el destino puede aceptar datos del objeto de datos, debe examinar **grfKeyState** para determinar si se han presionado las teclas modificadoras para modificar el comportamiento de colocación normal. Por ejemplo, la operación predeterminada suele ser un movimiento, pero la despresión de la tecla CTRL suele indicar una operación de copia.

Mientras el cursor está sobre la ventana [](#using-the-drag-and-drop-helper-object) de destino, el destino puede usar el objeto auxiliar de arrastrar y colocar para reemplazar la imagen de arrastre del objeto de datos por la suya propia. Si es así, [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) debe llamar a [**IDropTargetHelper::D ragEnter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) para pasar la información contenida en los parámetros *DragEnter* al objeto auxiliar de arrastrar y colocar.

### <a name="dragover-method"></a>Método DragOver

A medida que el cursor se mueve dentro de la ventana de destino, el sistema llama periódicamente al [**método IDropTarget::D ragOver.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) Sus parámetros proporcionan al destino la ubicación del cursor y el estado de las teclas modificadoras de teclado, como la tecla CTRL. **IDropTarget::D ragOver** tiene las mismas responsabilidades que [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)y las implementaciones suelen ser muy similares.

Si el destino usa el objeto auxiliar de arrastrar y colocar, [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) debe llamar a [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) para reenviar la información contenida en los parámetros *DragOver* al objeto auxiliar de arrastrar y colocar.

### <a name="drop-method"></a>Método Drop

El sistema llama al [**método IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) para notificar al destino que el usuario ha eliminado los datos, normalmente mediante la liberación del botón del mouse. **IDropTarget::D rop** tiene los mismos parámetros que [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). Normalmente, el destino responde mediante la extracción de uno o varios formatos del objeto de datos. Cuando termine, el destino debe establecer el *parámetro pdwEffect* en un [**valor DROPEFFECT**](../com/dropeffect-constants.md) que indique el resultado de la operación. Para algunos tipos de transferencia de datos de Shell, el destino también debe llamar a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para pasar un formato con información adicional sobre el resultado de la operación al objeto de datos. Para obtener una explicación detallada, vea [Handling Shell Data Transfer Scenarios](datascenarios.md).

Si el destino usa el objeto auxiliar de arrastrar y colocar, [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) debe llamar a [**IDropTargetHelper::D rop**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) para reenviar la información contenida en los parámetros [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) al objeto auxiliar de arrastrar y colocar.

## <a name="using-the-drag-and-drop-helper-object"></a>Usar el objeto auxiliar de arrastrar y colocar

El shell exporta el objeto auxiliar de arrastrar y colocar (CLSID DragDropHelper) para permitir que los destinos especifiquen la imagen de arrastre mientras está sobre la ventana \_ de destino. Para usar el objeto auxiliar de arrastrar y colocar, cree un objeto de servidor en proceso llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un identificador de clase (CLSID) de CLSID \_ DragDropHelper. El objeto auxiliar de arrastrar y colocar expone dos interfaces que se usan de la siguiente manera:

-   La [**interfaz IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) permite que el destino de colocación especifique un icono para representar el objeto de datos.
-   La [**interfaz IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permite que el destino de colocación informe al objeto auxiliar de arrastrar y colocar de la ubicación del cursor y mostrar u ocultar el icono de datos.

### <a name="using-the-idragsourcehelper-interface"></a>Uso de la interfaz IDragSourceHelper

El objeto auxiliar de arrastrar y colocar expone la interfaz [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) para permitir que un destino de colocación proporcione la imagen que se mostrará mientras el cursor está sobre la ventana de destino. **IDragSourceHelper proporciona** dos maneras alternativas de especificar el mapa de bits que se usará como imagen de arrastre:

-   Los destinos de colocación que tienen una ventana pueden registrar un mensaje de ventana DI GETDRAGIMAGE para él inicializando el objeto auxiliar de arrastrar y colocar con \_ [**IDragSourceHelper::InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Cuando el destino recibe un mensaje DI GETDRAGIMAGE, el controlador coloca la información de mapa de bits de la imagen de arrastre en la \_ [**estructura SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) que se pasa como el valor *lParam del* mensaje.
-   Los destinos de colocación sin ventanas especifican un mapa de bits cuando inicializan el objeto auxiliar de arrastrar y colocar [**con IDragSourceHelper::InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap).

### <a name="using-the-idroptargethelper-interface"></a>Uso de la interfaz IDropTargetHelper

Esta interfaz permite que el destino de colocación notifique al objeto auxiliar de arrastrar y colocar cuando el cursor entra o sale del destino. Mientras el cursor está sobre la ventana de destino, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permite al destino proporcionar al objeto auxiliar de arrastrar y colocar la información que el destino recibe a través de su [**interfaz IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

Cuatro de los métodos [**IDropTargetHelper:**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) [**IDropTargetHelper::D ragEnter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper::D ragLeave,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave) [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)y [**IDropTargetHelper::D rop)**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop)están asociados al método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del mismo nombre. Para usar el objeto auxiliar de arrastrar y colocar, cada uno de los métodos **IDropTarget** debe llamar al método **IDropTargetHelper** correspondiente para reenviar la información al objeto auxiliar de arrastrar y colocar. El quinto **método IDropTargetHelper,** [**IDropTargetHelper::Show,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show)notifica al objeto auxiliar de arrastrar y colocar que muestre u oculte la imagen de arrastre. Este método se usa al arrastrar sobre una ventana de destino en un modo de vídeo de baja profundidad de color. Permite que el destino oculte la imagen de arrastre mientras pinta la ventana.

 

 
