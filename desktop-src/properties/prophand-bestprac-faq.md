---
description: En este artículo se incluyen procedimientos recomendados y preguntas más frecuentes sobre cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5605c39f1021fcfe91259405bb99f8981510d3dc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405958"
---
# <a name="property-handler-best-practices-and-faq"></a>Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades

En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados](#property-handler-best-practices-and-faq)
    -   [Invalidar las propiedades del sistema de archivos](#overriding-file-system-properties)
    -   [Almacenar propiedades en formatos de archivo basados en XML](#storing-properties-in-xml-based-file-formats)
    -   [Propiedades calculadas](#computed-properties)
-   [Preguntas más frecuentes](#property-handler-best-practices-and-faq)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Prácticas recomendadas

Los procedimientos recomendados que se describen aquí proporcionan sugerencias de implementación útiles.

### <a name="overriding-file-system-properties"></a>Invalidar las propiedades del sistema de archivos

Algunas propiedades de los archivos las proporciona el origen de datos del sistema de archivos, como:

-   PKEY \_ FileName
-   Extensión \_ PKEY
-   PKEY \_ ModifiedTime

En general, los controladores de propiedades no pueden proporcionar valores para estas propiedades. Sin embargo, en algunos casos estas propiedades se pueden invalidar en función de la información de registro proporcionada por el controlador de propiedades. Los controladores de propiedades rellenan **HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{handler clsid}* \\ **OverrideFileSystemProperties** con los nombres de las propiedades que quieren invalidar. Esto se limita a un conjunto fijo de propiedades que se muestran en la siguiente lista de las que el sistema tiene conocimientos.

La invalidación se admite para los siguientes valores de propiedad:

-   [System.Kind](./props-system-kind.md)
-   [System.FileName](./props-system-filename.md)
-   [System.IsPinnedToNameSpaceTree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System.SFGAOFlags](./props-system-sfgaoflags.md)
-   [System.ItemPathDisplay](./props-system-itempathdisplay.md)
-   [System.ItemPathDisplayNarrow](./props-system-itempathdisplaynarrow.md)
-   [System.ItemFolderNameDisplay](./props-system-itemfoldernamedisplay.md)
-   [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)
-   [System.ItemFolderPathDisplayNarrow](./props-system-itemfolderpathdisplaynarrow.md)

Para obtener una lista completa de todas las propiedades de Shell, vea [Propiedades del shell.](./props.md)

> [!IMPORTANT]
> Los valores de propiedad invalidados solo se usan cuando se indexan los archivos. Por lo tanto, la exploración de archivos desde el origen de datos del sistema de archivos no revela los valores invalidados.

 

### <a name="storing-properties-in-xml-based-file-formats"></a>Almacenar propiedades en formatos de archivo basados en XML

Hay dos opciones básicas disponibles para almacenar propiedades en formatos de archivo basados en XML:

-   Almacene cada propiedad mediante elementos y atributos XML según el esquema XML del documento. Este enfoque es más "descriptivo para XML".
-   Serializa todo el almacén de propiedades en un objeto binario grande (BLOB) de memoria, convierte el BLOB en una cadena codificada en base64 y, a continuación, almacena esa cadena en el XML. Este es el más sencillo de los dos enfoques y se puede usar para proporcionar compatibilidad trivial con metadatos abiertos.

Algunos controladores pueden combinar estos enfoques, almacenar algunos valores importantes en formato XML estándar y almacenar el resto en un BLOB, por ejemplo.

### <a name="computed-properties"></a>Propiedades calculadas

Algunas propiedades se derivan de atributos específicos de un archivo. Por ejemplo, la [propiedad System.Image.Dimensions](./props-system-image-dimensions.md) viene determinada por las dimensiones reales de la imagen en un archivo de imagen. Dado que el controlador de propiedades no puede cambiar estos valores de propiedad, se marcan en `isInnate="true"` la descripción de la propiedad. Otras propiedades se calculan a partir de una parte de una propiedad específica o agregando los valores de varias propiedades. Dado que las actualizaciones de estas propiedades "calculadas" crearían ambigüedad en cuanto a cómo se deben cambiar los valores de "origen", las propiedades calculadas deben marcarse en la descripción de la propiedad o notificadas como de solo `isInnate="true"` lectura. La última opción está disponible indicando al controlador que devuelva S \_ FALSE de [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable).

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

En esta sección se proporcionan respuestas a las preguntas más frecuentes sobre propiedades y controladores de propiedades, así como respuestas que lo acompañan.

-   **Pregunta:** ¿Por qué el indexador no carga mi controlador de propiedades Windows Search propiedad?

    El Windows Search se ejecuta como un servicio del sistema y no puede cargar archivos DLL almacenados en el directorio de perfil de usuario. Si va a compilar y depurar mediante Microsoft Visual Studio, colocará el archivo DLL en el perfil de usuario (y, por lo tanto, el indexador no lo cargará). Para evitar este problema, copie el archivo DLL fuera de la carpeta de perfil (por ejemplo, en C: Archivos de programa **\\ \\ YourAppName)** y regístrelo allí.

    Para obtener instrucciones más específicas sobre cómo desarrollar controladores de propiedades para trabajar con el indexador Windows Search, vea [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

-   **Pregunta:** ¿Qué propiedades se deben detectar mediante los métodos de enumeración [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) [**e IPropertyStore::GetAt?**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))

    No todos los clientes de objetos de almacén de propiedades usan estos métodos. Algunos clientes son conscientes de las propiedades que planean solicitar directamente (por nombre PKEY) o reciben información de propiedades a través de una lista de descripción de propiedades. Los métodos de detección de propiedades suppport varios otros escenarios. Si una propiedad no necesita participar en estos escenarios, no es necesario enumerarse. Por lo tanto, un controlador de propiedades puede generar un valor EMPTY que no sea VT para las propiedades que no se detectan a través de los métodos \_ [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) [**e IPropertyStore::GetAt.**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))

    Sin embargo, las propiedades deben ser visibles a través de estos métodos si se cumple alguna de las condiciones siguientes:

    -   **Si la propiedad está indexada para que se pueda buscar:** Esto significa que se incluye en el almacén de propiedades Windows Search (lo indica en el esquema de descripción de la propiedad) o está disponible para las búsquedas de `isColumn = "true"` texto completo ( `inInvertedIndex = "true"` ). En ausencia de estas marcas o la ausencia de una descripción de propiedad, las propiedades de tipo "cadena" se agregarán automáticamente al índice invertido para habilitar la búsqueda. Dado que la lista de propiedades conocidas (aquellas con descripciones de propiedades instaladas) en el sistema de propiedades es muy grande (más de 800 propiedades), sería poco práctico pedir a cada controlador de propiedades todas las propiedades registradas en el sistema de propiedades. En su lugar, el proceso de indexación enumera las propiedades pertinentes del controlador de propiedades para cada elemento que indexa y usa los valores de las propiedades enumeradas para generar el índice de texto completo.
    -   **Si se debe copiar la propiedad cuando se duplica el conjunto** de propiedades del elemento: Para implementar una función "copiar un conjunto de propiedades", el elemento de origen hace que las propiedades que se deben copiar sean visibles a través de los métodos [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore::GetAt.**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) No se deben incluir las propiedades que no necesitan copiarse o que no tienen sentido copiar.
    -   **Si el valor de propiedad no está vacío (VT \_ EMPTY):** los valores de propiedad que están vacíos no son útiles para los clientes. Cuando los clientes intentan devolver valores de propiedad vacíos, se devuelve un valor de VT \_ EMPTY. Por lo tanto, no se deben enumerar las propiedades con valores vacíos.
    -   **Si se debe quitar la propiedad al invocar la función "quitar propiedades":** Esta característica existe para proteger la privacidad; detecta todos los valores del controlador de propiedades a través de la enumeración y quita cada uno de los valores seleccionados para su eliminación por el usuario.
        > [!Note]  
        > La enumeración de propiedades no comunica el conjunto de propiedades que admite un controlador de propiedades determinado si el controlador admite un esquema fijo (y no metadatos abiertos). En su lugar, estos controladores deben documentar el conjunto de propiedades que admiten.

         

-   **Pregunta:** Cómo saber qué formatos de archivo admiten metadatos abiertos?

    Para obtener información sobre la compatibilidad con metadatos abiertos, vea "Tipos de archivo que admiten metadatos abiertos" en [Tipos de archivo](../shell/fa-file-types.md).

-   **Pregunta:** ¿Se pueden almacenar valores NULL de VT \_ mediante un controlador de propiedades?

    No. Los valores NULL de VT se convertirán a VT EMPTY en las llamadas a \_ \_ [**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) e [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Pregunta:** ¿Qué formatos de cadena de fecha son [**compatibles con la función PropVariantChangeType?**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype)

    Por lo general, las propiedades que representan valores de fecha y hora se deben representar mediante VT \_ FILETIME. Sin embargo, muchos orígenes de datos proporcionan esta información en forma de cadena. La API auxiliar [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) admite la coerción de algunos formatos de fecha de cadena en valores [**FILETIME,**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) como se muestra en la tabla siguiente.

    

    | Formato                  | Windows Vista, Windows XP y Microsoft Windows Desktop Search (WDS) | Windows 7 | Notas                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | yyyy/mm/dd:hh:mm:ss.uuu | Sí                                                                   | Sí       | UTC; y=year, m=month, d=date, h=hours (reloj de 24 horas), m=minutes, s=seconds, u=microseconds                                                                                                           |
    | yyyy-mm-ddThh:mm:ssZ    | No                                                                    | Sí       | **Especificación de formato ISO8601** UTC (se indica mediante el indicador de zona horaria "Z"); y=year, m=month, d=date, h=hours (reloj de 24 horas), m=minutes, s=seconds; 'T' es un delimitador para la parte de tiempo.<br/> |

    

     

-   **Pregunta:** ¿Es posible crear un controlador de propiedades de solo lectura?

    Sí. Algunas implementaciones del controlador de propiedades no admiten la escritura de valores de propiedad. Estos controladores de propiedades deben devolver STGM E ACCESSDENIED en las llamadas a \_ \_ **IInitializeXXX::Initialize** que pasan STGM READWRITE o en cualquier llamada a \_ [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

    Todos los controladores de propiedades abiertos en el modo READ de STGM deben devolver \_ STGM E ACCESSDENIED en las llamadas \_ a \_ [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Pregunta:** ¿Puede un controlador de propiedades tratar una propiedad como de solo lectura, incluso si el esquema indica que la propiedad es de escritura?

    Sí. En el sistema de esquema, las propiedades se anotan como de solo lectura (incluidas las que tienen `isInnate = "true"` ) o de lectura y escritura. Los controladores de propiedades que no admiten la escritura de una propiedad determinada que el esquema dice que debe poder escribirse deben implementar [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) y devolver S FALSE en las llamadas a \_ [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) para esa propiedad. Esto indica que, en el contexto de este controlador y este archivo, la propiedad no se puede escribir.

    > [!Note]  
    > La acción inversa no es posible. No se puede permitir que un controlador de propiedades escriba una propiedad marcada como de solo lectura en el esquema

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicialización de controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registro y distribución de controladores de propiedades](./prophand-reg-dist.md)
</dt> </dl>

 

 
