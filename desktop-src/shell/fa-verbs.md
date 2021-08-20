---
description: Cuando un usuario hace clic con el botón derecho en un objeto shell, como un archivo, el Shell muestra un menú contextual.
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verbos y asociaciones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a144051b04ef2d9a2c9877b53e1680d4274afc92d3fc87fbcb531b02a0f94946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860798"
---
# <a name="verbs-and-file-associations"></a>Verbos y asociaciones de archivo

Cuando un usuario hace clic con el botón derecho en un objeto shell, como un archivo, el Shell muestra un menú contextual. Este menú contiene una lista de comandos que el usuario puede seleccionar para realizar varias acciones en el elemento. Estos comandos también se conocen como elementos de menú contextual o verbos. Los menús contextuales se pueden personalizar.

Este tema se organiza de la siguiente manera:

-   [Introducción a los menús contextuales para objetos del sistema de archivos](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Agregar comandos a un menú contextual](#add-commands-to-a-shortcut-menu)
-   [Verbos del menú contextual](#shortcut-menu-verbs)
-   [Transmitir elementos del sistema que no son de archivos y OpenSearch resultados.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrar una aplicación para controlar tipos de archivo arbitrarios](#register-an-application-to-handle-arbitrary-file-types)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Introducción a los menús contextuales para objetos del sistema de archivos

Dado que los menús contextuales se usan a menudo para la  administración de archivos, el Shell proporciona un conjunto de comandos predeterminados, como Cortar y Copiar **,** que aparecen en el menú contextual de cualquier objeto del sistema de archivos, como un archivo o una carpeta.

En el ejemplo siguiente se muestra un menú contextual predeterminado que se muestra haciendo clic con el **botón derecho MyFile.xyz-ms**.

![captura de pantalla del menú contextual predeterminado](images/context-menu/context-filesystemobjects.png)

La razón por la que aparece un menú contextual predeterminado para **MyFile.xyz-ms** se debe al hecho de que **.xyz-ms** no es miembro de un tipo de archivo registrado. Por el contrario, **.txt** es un tipo de archivo registrado. Si hace clic  con el botón derecho en un archivo.txt, verá un menú contextual  con tres comandos adicionales en su sección superior: **Imprimir,** **Editar y Abrir con**.

![captura de pantalla del menú contextual de un archivo con un tipo de archivo registrado](images/context-menu/context-registeredfiletype.png)

Para extender el menú contextual de un tipo de archivo, debe crear una entrada del Registro para cada comando. Un enfoque más sofisticado es implementar un controlador de menú contextual (verbo), que permite ampliar el menú contextual de un tipo de archivo archivo a archivo. Para obtener más información, vea [Crear controladores de menú contextual y](context-menu-handlers.md)Referencia del menú [contextual.](context-menu-reference.md)

### <a name="add-commands-to-a-shortcut-menu"></a>Agregar comandos a un menú contextual

Un controlador de menú contextual es un controlador de tipo de archivo que agrega comandos a un menú contextual existente. Los controladores de menús contextuales están asociados a un tipo de archivo y se llaman cada vez que se muestra un menú contextual para un miembro de la clase . El Shell comprueba el Registro para ver si el tipo de archivo está asociado a algún controlador de menú contextual. Si es así, el Shell consulta a los controladores si hay elementos de menú contextual adicionales.

## <a name="shortcut-menu-verbs"></a>Verbos del menú contextual

Cada comando del menú contextual se identifica en el Registro por su verbo. Estos verbos son los mismos que los que usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) al iniciar aplicaciones mediante programación.

Un verbo es una cadena de texto simple que el Shell usa para identificar el comando asociado. Cada verbo corresponde a la cadena de comando utilizada para iniciar el comando en una ventana de consola o un archivo por lotes (.bat).

Por ejemplo, el verbo abierto normalmente inicia un programa para abrir un archivo. La cadena de comando suele tener el siguiente aspecto:


```
"My Program.exe" "%1"
```



Si algún elemento de la cadena de comando contiene o puede contener espacios, debe incluirse entre comillas. De lo contrario, si el elemento contiene un espacio, no se analizará correctamente. Por ejemplo, **"My Program.exe"** inicia la aplicación correctamente. Si usa **My Program.exe** sin comillas, el sistema intenta iniciar **My** con **Program.exe** como primer argumento de línea de comandos. Siempre debe usar comillas con argumentos como **"%1"** que el Shell expande a cadenas, ya que no puede estar seguro de que la cadena no contendrá un espacio.

Los verbos también pueden tener un nombre para mostrar asociado a ellos, que se muestra en el menú contextual en lugar de la propia cadena de verbo. Por ejemplo, la cadena para mostrar de openas es **Open With**. Al igual que las cadenas de menú normales, incluir un carácter de yerba en la cadena de presentación permite la selección del teclado del comando.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Transmitir elementos del sistema que no son de archivos y OpenSearch resultados.

En Windows 7 y versiones posteriores, hay compatibilidad con la conexión de orígenes externos al cliente de Windows a través [del protocolo OpenSearch](http://www.opensearch.org/) cliente. Esto permite a los usuarios buscar en un almacén de datos remoto y ver los resultados desde Windows Explorer. El estándar OpenSearch v1.1 define formatos de archivo simples que se pueden usar para describir cómo un cliente debe consultar el servicio web para el almacén de datos y cómo debe devolver el servicio los resultados que el cliente debe representar.

Es posible que tenga que transmitir elementos que no son del [](http://www.opensearch.org/) sistema de archivos para evitar la necesidad de descargar elementos en el caso de OpenSearch resultados. La característica de búsqueda federada permite buscar elementos desde ubicaciones que no son del sistema de archivos que admiten OpenSearch, como SharePoint y otros sitios basados en servicios web, por ejemplo. Al invocar verbos en estos elementos, el sistema descarga una versión temporal del elemento y la pasa a la implementación del verbo. Se recomienda a los implementadores de verbos evitar la necesidad de descargar el archivo mediante el registro del conjunto de esquemas de dirección URL que admite el verbo para transmitir los elementos. Los verbos lo hacen mediante la clave del Registro **SupportedProtocols.**

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrar una aplicación para controlar tipos de archivo arbitrarios

Definir elementos de menú contextual para un tipo de archivo determinado permite especificar cómo la aplicación asociada abre un miembro del tipo de archivo. Sin embargo, las aplicaciones también pueden registrar un procedimiento predeterminado independiente que se usará cuando un usuario intente usar la aplicación para abrir un tipo de archivo que no está asociado a la aplicación. El procedimiento predeterminado se registra de la misma manera que se registran los elementos del menú contextual. Para obtener información más detallada sobre cómo definir elementos de menú contextual, vea [Crear controladores de menú contextual.](context-menu.md)

El procedimiento predeterminado tiene dos propósitos básicos. Una es especificar cómo se debe invocar la aplicación para abrir un tipo de archivo arbitrario. Por ejemplo, podría usar una marca de línea de comandos para indicar que se está abierto un tipo de archivo desconocido. El otro propósito es definir las distintas características de un tipo de archivo, como los elementos del menú contextual y el icono. Si un usuario asocia la aplicación a un tipo de archivo adicional, esa clase tendrá estas características. Si el tipo de archivo adicional se asoció previamente a otra aplicación, estas características reemplazarán a los originales.

Para registrar el procedimiento predeterminado, coloque las mismas claves del Registro que creó para el ProgID de la aplicación en la subclave de la aplicación de aplicaciones raíz **HKEY \_ CLASSES \_ \\**. También puede incluir un valor **FriendlyAppName** para proporcionar al sistema un nombre descriptivo para la aplicación. El nombre descriptivo de la aplicación también se puede extraer de su archivo ejecutable, pero solo si el valor FriendlyAppName está ausente.

En la siguiente entrada del Registro de ejemplo se muestra un procedimiento predeterminado **MyProgram.exe** que define un nombre descriptivo y varios elementos de menú contextual. Las cadenas de comando incluyen **la marca /a** para notificar a la aplicación que está abriendo un tipo de archivo arbitrario. Si incluye una subclave **DefaultIcon,** debe usar un icono genérico.

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

-   Para obtener información adicional, vea [Introducción a las asociaciones de archivo.](fa-intro.md)
-   Para obtener información conceptual sobre cómo extender el Shell con controladores de tipo de archivo, vea [Creating Shell Extension Handlers](handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple](verbs-best-practices.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Creación de controladores de menús contextuales](context-menu-handlers.md)
</dt> <dt>

[Personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menús contextuales](context-menu.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 



