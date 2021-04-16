---
description: Cuando un usuario hace clic con el botón secundario en un objeto de Shell, como un archivo, el shell muestra un menú contextual.
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verbos y asociaciones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b398b168afe66c3ddd1abe4c78863fbf67ffcbd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564518"
---
# <a name="verbs-and-file-associations"></a>Verbos y asociaciones de archivo

Cuando un usuario hace clic con el botón secundario en un objeto de Shell, como un archivo, el shell muestra un menú contextual. Este menú contiene una lista de comandos que el usuario puede seleccionar para realizar diversas acciones en el elemento. Estos comandos también se conocen como elementos de menú contextual o verbos. Los menús contextuales se pueden personalizar.

Este tema se organiza de la siguiente manera:

-   [Introducción a los menús contextuales para objetos del sistema de archivos](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Agregar comandos a un menú contextual](#add-commands-to-a-shortcut-menu)
-   [Verbos del menú contextual](#shortcut-menu-verbs)
-   [Transmitir elementos del sistema que no son de archivos y resultados de OpenSearch.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrar una aplicación para controlar tipos de archivo arbitrarios](#register-an-application-to-handle-arbitrary-file-types)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Introducción a los menús contextuales para objetos del sistema de archivos

Dado que los menús contextuales suelen usarse para la administración de archivos, el Shell proporciona un conjunto de comandos predeterminados, como **cortar** y **copiar**, que aparecen en el menú contextual de cualquier objeto del sistema de archivos, como un archivo o una carpeta.

En el ejemplo siguiente se muestra un menú contextual predeterminado que se muestra al hacer clic con el botón secundario en **myFile.XYZ-MS**.

![captura de pantalla del menú contextual predeterminado](images/context-menu/context-filesystemobjects.png)

La razón por la que aparece un menú contextual predeterminado para **myFile.XYZ-MS** se debe al hecho de que **. XYZ-MS** no es miembro de un tipo de archivo registrado. Por el contrario, **. txt** es un tipo de archivo registrado. Si hace clic con el botón secundario en un archivo **. txt** , verá un menú contextual con tres comandos adicionales en la sección superior: **Imprimir**, **Editar** y **abrir con**.

![captura de pantalla del menú contextual de un archivo con un tipo de archivo registrado](images/context-menu/context-registeredfiletype.png)

Para extender el menú contextual de un tipo de archivo, debe crear una entrada del registro para cada comando. Un enfoque más sofisticado consiste en implementar un controlador de menú contextual (verbo), que le permite extender el menú contextual de un tipo de archivo cada archivo. Para obtener más información, vea [crear controladores de menús contextuales](context-menu-handlers.md)y [Referencia del menú contextual](context-menu-reference.md).

### <a name="add-commands-to-a-shortcut-menu"></a>Agregar comandos a un menú contextual

Un controlador de menú contextual es un controlador de tipo de archivo que agrega comandos a un menú contextual existente. Los controladores de menú contextual están asociados a un tipo de archivo y se les llama siempre que se muestra un menú contextual para un miembro de la clase. El shell comprueba el registro para ver si el tipo de archivo está asociado a los controladores de menú contextuales. Si es así, el shell consulta los controladores de los elementos de menú contextual adicionales.

## <a name="shortcut-menu-verbs"></a>Verbos del menú contextual

Cada comando del menú contextual se identifica en el registro mediante su verbo. Estos verbos son los mismos que los utilizados por [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) al iniciar aplicaciones mediante programación.

Un verbo es una cadena de texto simple que el shell usa para identificar el comando asociado. Cada verbo corresponde a la cadena de comandos que se usa para iniciar el comando en una ventana de la consola o en un archivo por lotes (. bat).

Por ejemplo, el verbo abrir normalmente inicia un programa para abrir un archivo. La cadena de comandos suele tener el siguiente aspecto:


```
"My Program.exe" "%1"
```



Si algún elemento de la cadena de comandos contiene o puede contener espacios, debe escribirse entre comillas. De lo contrario, si el elemento contiene un espacio, no se analizará correctamente. Por ejemplo, **"My Program.exe"** inicia la aplicación correctamente. Si usa **mi Program.exe** sin comillas, el sistema intenta iniciar **My** con **Program.exe** como su primer argumento de la línea de comandos. Siempre debe usar comillas con argumentos como **"%1**" que se expandan a cadenas mediante el Shell, ya que no puede estar seguro de que la cadena no contendrá un espacio.

Los verbos también pueden tener un nombre para mostrar asociado, que se muestra en el menú contextual en lugar de la propia cadena de verbo. Por ejemplo, la cadena de presentación para openas está **abierta con**. Al igual que las cadenas de menú normales, incluir un carácter de y comercial en la cadena de presentación permite la selección del teclado del comando.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Transmitir elementos del sistema que no son de archivos y resultados de OpenSearch.

En Windows 7 y versiones posteriores, hay compatibilidad con la conexión de orígenes externos con el cliente de Windows a través del protocolo [OpenSearch](http://www.opensearch.org/) . Esto permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde el explorador de Windows. El estándar de OpenSearch v 1.1 define formatos de archivo simples que se pueden usar para describir cómo un cliente debe consultar el servicio web para el almacén de datos y cómo el servicio debe devolver los resultados que el cliente va a representar.

Es posible que necesite transmitir por secuencias elementos del sistema que no son de archivos para evitar la necesidad de descargar elementos en el caso de los resultados de [OpenSearch](http://www.opensearch.org/) . La característica de búsqueda federada permite buscar elementos desde ubicaciones del sistema que no son de archivos que admiten OpenSearch, como SharePoint y otros sitios respaldados por servicios Web, por ejemplo. Al invocar verbos en estos elementos, el sistema descarga una versión temporal del elemento y la pasa a la implementación del verbo. Se recomienda a los implementadores de verbo evitar la necesidad de descargar el archivo registrando el conjunto de esquemas de dirección URL que admite el verbo para transmitir los elementos. Los verbos lo hacen mediante la clave del registro **SupportedProtocols** .

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrar una aplicación para controlar tipos de archivo arbitrarios

La definición de los elementos de menú contextual para un tipo de archivo determinado le permite especificar cómo abre la aplicación asociada un miembro del tipo de archivo. Sin embargo, las aplicaciones también pueden registrar un procedimiento predeterminado independiente que se utilizará cuando un usuario intente usar la aplicación para abrir un tipo de archivo que no esté asociado a la aplicación. El procedimiento predeterminado se registra prácticamente de la misma manera que se registran los elementos de menú contextual. Para obtener información más detallada sobre cómo definir los elementos de menú contextual, vea [crear controladores de menús contextuales](context-menu.md).

El procedimiento predeterminado sirve para dos propósitos básicos. Uno consiste en especificar cómo se debe invocar la aplicación para abrir un tipo de archivo arbitrario. Por ejemplo, podría usar una marca de línea de comandos para indicar que se está abriendo un tipo de archivo desconocido. El otro propósito es definir las distintas características de un tipo de archivo, como los elementos de menú contextual y el icono. Si un usuario asocia su aplicación con un tipo de archivo adicional, esa clase tendrá estas características. Si el tipo de archivo adicional estaba asociado previamente a otra aplicación, estas características reemplazarán a los originales.

Para registrar el procedimiento predeterminado, coloque las mismas claves del registro que creó para el ID. de programa de la aplicación en la subclave de la aplicación de las **\_ \_ \\ aplicaciones raíz HKEY**. También puede incluir un valor de **FriendlyAppName** para proporcionar al sistema un nombre descriptivo para la aplicación. También se puede extraer el nombre descriptivo de la aplicación de su archivo ejecutable, pero solo si el valor de FriendlyAppName no está presente.

En la entrada del registro de ejemplo siguiente se muestra un procedimiento predeterminado para **MyProgram.exe** que define un nombre descriptivo y varios elementos de menú contextual. Las cadenas de comandos incluyen la marca **/a** para notificar a la aplicación que está abriendo un tipo de archivo arbitrario. Si incluye una subclave **DefaultIcon** , debe usar un icono genérico.

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a>Recursos adicionales

-   Para más información, consulte [Introducción a las asociaciones de archivo](fa-intro.md).
-   Para obtener información conceptual sobre cómo extender el shell con controladores de tipo de archivo, vea [crear controladores de extensión de Shell](handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección](verbs-best-practices.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Crear controladores de menú contextual](context-menu-handlers.md)
</dt> <dt>

[Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menú contextual](context-menu.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 



