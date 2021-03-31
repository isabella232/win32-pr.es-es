---
description: En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5188e66f08f3c6cf449f8bc61feb6aac829d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278909"
---
# <a name="property-handler-best-practices-and-faq"></a>Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades

En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados](#property-handler-best-practices-and-faq)
    -   [Invalidar propiedades del sistema de archivos](#overriding-file-system-properties)
    -   [Almacenar propiedades en formatos de archivo basados en XML](#storing-properties-in-xml-based-file-formats)
    -   [Propiedades calculadas](#computed-properties)
-   [Preguntas más frecuentes](#property-handler-best-practices-and-faq)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Prácticas recomendadas

Los procedimientos recomendados que se describen aquí proporcionan sugerencias de implementación útiles.

### <a name="overriding-file-system-properties"></a>Invalidar propiedades del sistema de archivos

El origen de datos del sistema de archivos proporciona algunas propiedades para los archivos, como:

-   \_Nombre de archivo PKEY
-   \_Extensión PKEY
-   PKEY \_ ModifiedTime

En general, los controladores de propiedad no pueden proporcionar valores para estas propiedades. Sin embargo, en algunos casos estas propiedades se pueden invalidar según la información de registro proporcionada por el controlador de propiedades. Los controladores de propiedades rellenan **\_ las clases HKEY \_ raíz** \\ **CLSID** \\ *{handler}* \\ **OverrideFileSystemProperties** con los nombres de las propiedades que desea invalidar. Esto se limita a un conjunto fijo de propiedades que se muestran en la siguiente lista de la que el sistema tiene conocimiento.

Se admite la invalidación para los siguientes valores de propiedad:

-   [System. Kind](./props-system-kind.md)
-   [System. FileName](./props-system-filename.md)
-   [System. IsPinnedToNameSpaceTree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System. SFGAOFlags](./props-system-sfgaoflags.md)
-   [System. ItemPathDisplay](./props-system-itempathdisplay.md)
-   [System. ItemPathDisplayNarrow](./props-system-itempathdisplaynarrow.md)
-   [System. ItemFolderNameDisplay](./props-system-itemfoldernamedisplay.md)
-   [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)
-   [System. ItemFolderPathDisplayNarrow](./props-system-itemfolderpathdisplaynarrow.md)

Para obtener una lista completa de todas las propiedades de Shell, consulte [propiedades de Shell](./props.md).

> [!IMPORTANT]
> Los valores de propiedad invalidados solo se usan cuando se indizan los archivos. Por lo tanto, la exploración de archivos desde el origen de datos del sistema de archivos no revela los valores invalidados.

 

### <a name="storing-properties-in-xml-based-file-formats"></a>Almacenar propiedades en formatos de archivo basados en XML

Hay dos opciones básicas disponibles para almacenar propiedades en formatos de archivo basados en XML:

-   Almacene cada propiedad utilizando elementos y atributos XML según el esquema XML del documento. Este enfoque es más "descriptivo para XML".
-   Serialice el almacén de propiedades completo en un objeto binario grande (BLOB) de memoria, convierta el BLOB en una cadena codificada en Base64 y, a continuación, almacene esa cadena en el XML. Este es el más sencillo de los dos enfoques y se puede usar para proporcionar de forma trivial compatibilidad con los metadatos abiertos.

Algunos controladores pueden combinar estos enfoques, almacenar algunos valores importantes en formato XML estándar y almacenar el resto en un BLOB, por ejemplo.

### <a name="computed-properties"></a>Propiedades calculadas

Algunas propiedades se derivan de atributos específicos de un archivo. Por ejemplo, la propiedad [System. Image. Dimensions](./props-system-image-dimensions.md) viene determinada por las dimensiones reales de la imagen en un archivo de imagen. Dado que el controlador de la propiedad no puede cambiar estos valores de propiedad, se marcan por tanto `isInnate="true"` en la descripción de la propiedad. Otras propiedades se calculan a partir de una parte de una propiedad específica o agregando los valores de varias propiedades. Debido a que las actualizaciones de estas propiedades "calculadas" deberían crear ambigüedad en lo que respecta al modo en que se deben cambiar los valores de "origen", las propiedades calculadas deben marcarse `isInnate="true"` en la descripción de la propiedad o se pueden informar como de solo lectura. Esta última opción está disponible indicando al controlador que devuelva S \_ false desde [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable).

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

En esta sección se proporcionan respuestas a las preguntas más frecuentes sobre las propiedades y los controladores de propiedades, y las respuestas que lo acompañan.

-   **Pregunta:** ¿Por qué el indizador de Windows Search no carga mi controlador de propiedades?

    El indizador de Windows Search se ejecuta como un servicio del sistema y no puede cargar los archivos dll almacenados en el directorio del perfil de usuario. Si va a compilar y depurar mediante Microsoft Visual Studio, colocará el archivo DLL en el perfil de usuario (y, por tanto, el indexador no lo cargará). Para solucionar este error, copie la DLL fuera de la carpeta de su perfil (por ejemplo, en **C: \\ archivos de programa \\ YourAppName**) y regístrela en ella.

    Para obtener instrucciones más específicas sobre cómo desarrollar controladores de propiedades para trabajar con el indizador de Windows Search, vea [desarrollar controladores de propiedades para Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

-   **Pregunta:** ¿Qué propiedades deben detectarse mediante los métodos de enumeración [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) y [**IPropertyStore:: getadt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) ?

    No todos los clientes de objetos de almacén de propiedades usan estos métodos. Algunos clientes son conscientes de las propiedades que tienen previsto solicitar directamente (por nombre de PKEY) o recibir información de propiedades a través de una lista de descripción de propiedad. Los métodos de detección de propiedades soporte técnico varios otros escenarios. Si no es necesario que una propiedad participe en estos escenarios, no es necesario enumerarla. Por lo tanto, un controlador de propiedades puede generar un valor vacío que no sea de VT \_ para las propiedades que no se detectan a través de los métodos [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) y [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) .

    Sin embargo, las propiedades deberían estar visibles a través de estos métodos si se cumple alguna de las siguientes condiciones:

    -   **Si la propiedad está indizada para poder realizar búsquedas:** Esto significa que se incluye en el almacén de propiedades de búsqueda de Windows (indicado por `isColumn = "true"` en el esquema de descripción de la propiedad) o disponible para búsquedas de texto completo ( `inInvertedIndex = "true"` ). En ausencia de estas marcas o de la ausencia de una descripción de propiedad, las propiedades de tipo "String" se agregarán automáticamente al índice invertido para habilitar la búsqueda. Dado que la lista de propiedades conocidas (aquellas con las descripciones de propiedades instaladas) en el sistema de propiedades es muy grande (más de 800 propiedades), no sería práctico preguntar a cada controlador de propiedad para cada propiedad registrada en el sistema de propiedades. En su lugar, el proceso de indización enumera las propiedades pertinentes del controlador de propiedades para cada elemento que indexa y usa los valores de las propiedades enumeradas para generar el índice de texto completo.
    -   **Si se debe copiar la propiedad cuando el conjunto de propiedades del elemento está duplicado:** Para implementar una función "copiar conjunto de propiedades", el elemento de origen hace que las propiedades que se deben copiar sean visibles a través de los métodos [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) y [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) . No se deben incluir las propiedades que no es necesario copiar o que no tienen sentido copiar.
    -   **Si el valor de la propiedad no está vacío (VT \_ vacío):** los valores de propiedad que están vacíos no son útiles para los clientes. Cuando los clientes intentan devolver valores de propiedad vacíos, se devuelve un valor de VT \_ Empty. Por lo tanto, no se deben enumerar las propiedades con valores vacíos.
    -   **Si se debe quitar la propiedad al invocar la función "quitar propiedades":** Esta característica existe para proteger la privacidad; detecta todos los valores del controlador de propiedad a través de la enumeración y quita cada uno seleccionado para su eliminación por parte del usuario.
        > [!Note]  
        > Enumerar propiedades no comunica el conjunto de propiedades que admite un controlador de propiedad determinado si el controlador admite un esquema fijo (y no metadatos abiertos). En su lugar, estos controladores deben documentar el conjunto de propiedades que admiten.

         

-   **Pregunta:** Cómo saber qué formatos de archivo admiten metadatos abiertos?

    Para obtener información sobre la compatibilidad con los metadatos abiertos, vea "tipos de archivo que admiten metadatos abiertos" en [tipos de archivo](../shell/fa-file-types.md).

-   **Pregunta:** ¿ \_ Se pueden almacenar valores NULL de VT mediante un controlador de propiedad?

    No. \_Los valores NULL de VT se convertirán en VT \_ vacío en las llamadas a [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) y [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Pregunta:** ¿Qué formatos de cadena de fecha admite la función [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) ?

    Por lo general, las propiedades que representan valores de fecha y hora se deben representar con VT \_ FILETIME. Sin embargo, muchos orígenes de datos proporcionan esta información en forma de cadena. La API de la aplicación auxiliar [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) permite forzar algunos formatos de fecha de cadena en valores [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , tal como se muestra en la tabla siguiente.

    

    | Formato                  | Windows Vista, Windows XP y Microsoft Windows Desktop Search (WDS) | Windows 7 | Notas                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | aaaa/mm/dd: HH: mm: SS. UUU | Sí                                                                   | Sí       | UTC y = año, m = mes, d = fecha, h = horas (reloj de 24 horas), m = minutos, s = segundos, u = microsegundos                                                                                                           |
    | aaaa-mm-ddThh: mm: ssZ    | No                                                                    | Sí       | **Especificación de formato ISO8601** Hora UTC (indicada por el indicador de zona horaria "Z"); y = año, m = mes, d = fecha, h = horas (reloj de 24 horas), m = minutos, s = segundos; ' T ' es un delimitador para la parte de hora.<br/> |

    

     

-   **Pregunta:** ¿Es posible crear un controlador de propiedades de solo lectura?

    Sí. Algunas implementaciones del controlador de propiedad no admiten la escritura de valores de propiedad. Estos controladores de propiedades deben devolver STGM \_ E \_ ACCESSDENIED en las llamadas a **IInitializeXXX:: Initialize** que pasan STGM \_ ReadWrite o en cualquier llamada a [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

    Todos los controladores de propiedad abiertos en el \_ modo de lectura STGM deben devolver STGM \_ E \_ ACCESSDENIED en las llamadas a [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Pregunta:** ¿Un controlador de propiedades puede tratar una propiedad como de solo lectura, aunque el esquema indique que la propiedad es grabable?

    Sí. En el sistema de esquema, las propiedades se anotan como de solo lectura (incluidas aquellas con `isInnate = "true"` ) o de lectura/escritura. Los controladores de propiedades que no admiten la escritura de una propiedad determinada que el esquema indica deben ser de escritura deben implementar [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) y devolver S \_ false en las llamadas a [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) para esa propiedad. Esto indica que en el contexto de este controlador y este archivo, la propiedad no es grabable.

    > [!Note]  
    > La acción inversa no es posible. No se puede habilitar un controlador de propiedades para escribir una propiedad marcada como de solo lectura en el esquema

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md)
</dt> </dl>

 

 
