---
description: En este tema se describe qué son las bibliotecas y cómo pueden beneficiar a los usuarios y desarrolladores.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Acerca de las bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564870"
---
# <a name="about-libraries"></a>Acerca de las bibliotecas

En este tema se describe qué son las bibliotecas y cómo pueden beneficiar a los usuarios y desarrolladores.

Las bibliotecas son colecciones de carpetas definidas por el usuario. Una biblioteca realiza un seguimiento de la ubicación física de almacenamiento de cada carpeta, lo que libera al usuario y al software de esa tarea. Los usuarios pueden agrupar las carpetas relacionadas en una biblioteca aunque dichas carpetas estén almacenadas en diferentes unidades de disco duro o en equipos diferentes.

En una biblioteca, las carpetas y los archivos aparecen al usuario como una sola colección y, mediante la API de la biblioteca de Shell, el contenido de la biblioteca también puede aparecer en una única ubicación para un programa.

En una biblioteca, el contenido, como documentos, fotos, vídeos o música de un usuario, se puede ordenar y mostrar como el usuario desea y no simplemente como requiere el sistema de archivos. Por ejemplo, los usuarios pueden organizar el contenido de una biblioteca mediante las propiedades de los elementos de la biblioteca para que los elementos relacionados se ordenen juntos incluso si se almacenan en carpetas diferentes.

![captura de pantalla de la interfaz de usuario de bibliotecas](images/libraries-whatare.png)

En este tema:

-   [Ventajas de la biblioteca](#library-benefits)
    -   [Ventajas del usuario](#user-benefits)
    -   [Ventajas para desarrolladores](#developer-benefits)
-   [Administrar carpetas en bibliotecas](#managing-folders-in-libraries)
-   [Temas relacionados](#related-topics)

## <a name="library-benefits"></a>Ventajas de la biblioteca

En esta sección se describen algunas de las ventajas de las bibliotecas desde la perspectiva del usuario final y la perspectiva del desarrollador del programa.

### <a name="user-benefits"></a>Ventajas del usuario

La incorporación de compatibilidad con la biblioteca al programa proporciona las siguientes ventajas al usuario:

-   **Las bibliotecas proporcionan una interfaz de usuario coherente en Windows 7**

    Los cuadros de diálogo de archivos comunes admiten bibliotecas y proporcionan la misma experiencia de usuario que el explorador de Windows en Windows 7. Las bibliotecas auxiliares del programa le ayudarán a proporcionar una interacción más fluida para el usuario al usar el programa en Windows 7.

-   **Los usuarios deciden dónde almacenar el contenido**

    Las bibliotecas permiten a los usuarios controlar dónde se almacena su contenido. Al mismo tiempo, las bibliotecas proporcionan valores predeterminados razonables para los usuarios que no desean administrar dicho nivel de detalle en su equipo. Los usuarios deciden cuántos, o cuántos controlan, desean ejercitar dónde y cómo se almacena su contenido y la biblioteca funciona bien en cualquier caso.

### <a name="developer-benefits"></a>Ventajas para desarrolladores

Puede usar las bibliotecas de su programa para proporcionar una interfaz de usuario más flexible y cómoda sin tener que agregar una gran cantidad de código de programa complejo. Estas son algunas de las ventajas de agregar compatibilidad de biblioteca:

-   **Bibliotecas compatibles con el acceso a la biblioteca y al sistema de archivos**

    Con la [**API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)de la biblioteca de Shell, los programas pueden proporcionar compatibilidad de biblioteca al usuario a la vez que se reduce la complejidad del código de administración de archivos y carpetas. Si el programa ya usa la API del sistema de archivos, puede conservar todo el código existente que desee y, aun así, proporcionar al usuario la información necesaria para la biblioteca obteniendo la información necesaria del sistema de archivos de la API de la **biblioteca de Shell**.

-   **Notificación de cambio más sencilla**

    Tanto el sistema de archivos como la API de Shell pueden notificar al programa cuando cambia el contenido de una carpeta o biblioteca supervisada. Sin embargo, mediante la API de Shell, puede supervisar todas las carpetas de la biblioteca con una sola notificación, aunque la carpeta de la biblioteca se puede almacenar en unidades diferentes o incluso en equipos diferentes.

-   **Las bibliotecas usan propiedades de archivo**

    Los programas pueden usar las propiedades de archivo para controlar qué archivos se muestran durante las operaciones de apertura y guardado que usan los cuadros de diálogo de archivos comunes. Los programas también pueden tener acceso a las propiedades de archivo mediante el uso de las interfaces [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Los cuadros de diálogo de archivos comunes también se pueden configurar para permitir a los usuarios actualizar las propiedades que están asociadas con su contenido.

-   **Los programas pueden crear bibliotecas dedicadas**

    Se puede crear una nueva biblioteca cuando las bibliotecas de usuario existentes no satisfacen las necesidades del programa, por ejemplo, si un programa crea un nuevo tipo de contenido de usuario. La nueva biblioteca se puede configurar con un icono único que representa su contenido y facilita la identificación de la biblioteca en el explorador de Windows.

## <a name="managing-folders-in-libraries"></a>Administrar carpetas en bibliotecas

Los usuarios pueden organizar sus bibliotecas agregando, moviendo o quitando carpetas en la biblioteca. Sin embargo, no todas las carpetas admiten todas las funciones que puede proporcionar una biblioteca. Muchas características de la biblioteca requieren un acceso rápido a las distintas propiedades de la carpeta y su contenido que solo están disponibles a través de Windows Search. Para proporcionar toda la funcionalidad de la biblioteca, la búsqueda de Windows debe ser capaz de indexar una carpeta.

Una biblioteca no permite a un usuario agregar carpetas que no proporcionan funcionalidad completa de la biblioteca. Sin embargo, la API de la [**biblioteca de Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) puede agregar estas carpetas. Si una biblioteca contiene una carpeta que no admite la funcionalidad de biblioteca completa, la biblioteca funcionará en modo seguro y proporcionará una funcionalidad limitada. En la tabla siguiente se describen las carpetas que admiten la funcionalidad de la biblioteca completa y las que no lo hacen.



| Tipos de carpeta que admiten la funcionalidad de biblioteca completa                                                               | Tipos de carpeta que no admiten la funcionalidad de biblioteca completa                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Discos duros NTFS y FAT32 fijos y externos.                                                                     | Unidades extraíbles, como unidades flash USB o tarjetas de memoria Secure Digital (SD).               |
| Recursos compartidos de archivos que se indexan mediante Windows Search, como servidores departamentales, Windows 7 o equipos domésticos de Windows Vista. | Medios extraíbles, como CD-ROM o DVD.                                                 |
| Recursos compartidos de archivos que están disponibles sin conexión, como una carpeta redirigida **Mis documentos** o una memoria caché de Client-Side.        | Recursos compartidos de red que no están disponibles sin conexión ni indexados de forma remota, como las unidades NAS.   |
|                                                                                                                    | Otros orígenes de datos, como Microsoft SharePoint, Microsoft Exchange y Microsoft OneDrive. |



 

En la imagen siguiente se muestra la presentación limitada del contenido de la biblioteca en modo seguro.

![abrir el cuadro de diálogo cuando las bibliotecas están en modo seguro](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Vínculos de Shell](./links.md)
</dt> <dt>

[Carpetas conocidas](known-folders.md)
</dt> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> </dl>

 

 
