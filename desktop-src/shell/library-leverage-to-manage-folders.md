---
description: En este tema se describe qué son las bibliotecas y cómo pueden beneficiar a los usuarios y desarrolladores.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Acerca de las bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e63aef55513fb36f9a3cbfa71c1b7a79040fd7848468bd1216779cd034132d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049328"
---
# <a name="about-libraries"></a>Acerca de las bibliotecas

En este tema se describe qué son las bibliotecas y cómo pueden beneficiar a los usuarios y desarrolladores.

Las bibliotecas son colecciones de carpetas definidas por el usuario. Una biblioteca realiza un seguimiento de la ubicación de almacenamiento físico de cada carpeta, lo que libera al usuario y al software de esa tarea. Los usuarios pueden agrupar carpetas relacionadas en una biblioteca incluso si esas carpetas se almacenan en diferentes unidades de disco duro o equipos diferentes.

En una biblioteca, las carpetas y los archivos aparecen al usuario como una sola colección y, mediante la API de biblioteca de Shell, el contenido de la biblioteca también puede parecer estar en una sola ubicación para un programa.

En una biblioteca, el contenido, como los documentos, las fotos, los vídeos o la música de un usuario, se puede ordenar y mostrar como quiera el usuario y no simplemente como requiere el sistema de archivos. Por ejemplo, los usuarios pueden organizar el contenido de una biblioteca mediante las propiedades de los elementos de la biblioteca para que los elementos relacionados se ordenen juntos incluso si se almacenan en carpetas diferentes.

![captura de pantalla de la interfaz de usuario de las bibliotecas](images/libraries-whatare.png)

En este tema:

-   [Ventajas de la biblioteca](#library-benefits)
    -   [Ventajas del usuario](#user-benefits)
    -   [Ventajas para desarrolladores](#developer-benefits)
-   [Administración de carpetas en bibliotecas](#managing-folders-in-libraries)
-   [Temas relacionados](#related-topics)

## <a name="library-benefits"></a>Ventajas de la biblioteca

En esta sección se describen algunas de las ventajas de las bibliotecas desde la perspectiva del usuario final y la perspectiva del desarrollador del programa.

### <a name="user-benefits"></a>Ventajas del usuario

Agregar compatibilidad con bibliotecas al programa proporciona las siguientes ventajas al usuario:

-   **Las bibliotecas proporcionan una interfaz de usuario coherente en Windows 7**

    Los cuadros de diálogo de archivos comunes admiten bibliotecas y proporcionan la misma experiencia de usuario que Windows Explorer en Windows 7. La compatibilidad de las bibliotecas del programa le ayudará a proporcionar una interacción más fluida para el usuario al usar el programa en Windows 7.

-   **Los usuarios deciden dónde almacenar el contenido**

    Las bibliotecas permiten a los usuarios controlar dónde se almacena su contenido. Al mismo tiempo, las bibliotecas proporcionan valores predeterminados razonables para los usuarios que no desean administrar ese nivel de detalle en su equipo. Los usuarios deciden cuánto o qué poco quieren controlar sobre dónde y cómo se almacena su contenido, y la biblioteca funciona bien de cualquier manera.

### <a name="developer-benefits"></a>Ventajas para desarrolladores

Puede usar bibliotecas del programa para proporcionar una interfaz de usuario más flexible y cómoda sin tener que agregar mucho código de programa complejo. Algunas de las ventajas de agregar compatibilidad con bibliotecas incluyen:

-   **Las bibliotecas admiten el acceso a la biblioteca y al sistema de archivos**

    Con la [**API de biblioteca de Shell,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)los programas pueden proporcionar compatibilidad con la biblioteca para el usuario, a la vez que se reduce la complejidad de su código de administración de archivos y carpetas. Si el programa ya usa la API del sistema de archivos, puede conservar tanto código existente como desee y seguir proporcionando compatibilidad con la biblioteca al usuario obteniendo la información necesaria del sistema de archivos de la API de biblioteca de **Shell.**

-   **Notificación de cambios más sencilla**

    Tanto el sistema de archivos como la API de Shell pueden notificar al programa cuando cambia el contenido de una biblioteca o carpeta supervisada. Sin embargo, con shell API, puede supervisar todas las carpetas de la biblioteca con una única notificación, aunque la carpeta de la biblioteca se pueda almacenar en unidades diferentes o incluso en equipos diferentes.

-   **Las bibliotecas usan propiedades de archivo**

    Los programas pueden usar las propiedades de archivo para controlar qué archivos se muestran durante las operaciones de apertura y guardado que usan los cuadros de diálogo de archivos comunes. Los programas también pueden tener acceso a las propiedades de archivo mediante las [**interfaces IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) Los cuadros de diálogo de archivo comunes también se pueden configurar para permitir a los usuarios actualizar las propiedades asociadas a su contenido.

-   **Los programas pueden crear bibliotecas dedicadas**

    Se puede crear una nueva biblioteca cuando una biblioteca de usuario existente no satisface las necesidades del programa, por ejemplo, si un programa crea un nuevo tipo de contenido de usuario. La nueva biblioteca se puede configurar con un icono único que representa su contenido y facilita la identificación de la biblioteca en Windows Explorer.

## <a name="managing-folders-in-libraries"></a>Administración de carpetas en bibliotecas

Los usuarios pueden organizar sus bibliotecas agregando, moviendo o quitando carpetas de la biblioteca. Sin embargo, no todas las carpetas admiten toda la funcionalidad que puede proporcionar una biblioteca. Muchas características de biblioteca requieren acceso rápido a las distintas propiedades de la carpeta y su contenido que solo están disponibles a través de Windows Search. Para proporcionar la funcionalidad completa de la biblioteca, una carpeta debe ser capaz de indexarse mediante Windows Search.

Una biblioteca no permite a un usuario agregar carpetas que no proporcionan la funcionalidad completa de la biblioteca. Sin [**embargo, la API de**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) biblioteca de Shell puede agregar dichas carpetas. Si una biblioteca contiene una carpeta que no admite la funcionalidad de biblioteca completa, la biblioteca funcionará en modo seguro y proporcionará una funcionalidad limitada. En la tabla siguiente se describen las carpetas que admiten la funcionalidad completa de la biblioteca y las que no.



| Tipos de carpeta que admiten la funcionalidad de biblioteca completa                                                               | Tipos de carpeta que no admiten la funcionalidad de biblioteca completa                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Unidades de disco duro NTFS y FAT32 fijas y externas.                                                                     | Unidades extraíbles, como unidades flash USB o tarjetas de memoria Digital segura (SD).               |
| Recursos compartidos de archivos indexados por Windows Search, como servidores de departamento, Windows 7 o Windows equipos de inicio de Vista. | Medios extraíbles, como cd-ROM o medios de DVD.                                                 |
| Recursos compartidos de archivos que están disponibles sin conexión, como una carpeta **Mis documentos** redirigida o una Client-Side caché.        | Recursos compartidos de red que no están disponibles sin conexión ni indexados de forma remota, como unidades NAS.   |
|                                                                                                                    | Otros orígenes de datos, como Microsoft SharePoint, Microsoft Exchange y Microsoft OneDrive. |



 

En la imagen siguiente se muestra la presentación limitada del contenido de la biblioteca en modo seguro.

![abrir cuadro de diálogo cuando las bibliotecas están en modo seguro](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Vínculos de shell](./links.md)
</dt> <dt>

[Carpetas conocidas](known-folders.md)
</dt> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> </dl>

 

 
