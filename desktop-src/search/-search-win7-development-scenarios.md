---
description: Describe la introducción de bibliotecas para Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Bibliotecas de Shell de Windows en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb94551d80d0230966626f1bd6499801aff889c4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105689608"
---
# <a name="windows-shell-libraries-in-windows"></a>Bibliotecas de Shell de Windows en Windows

En este tema se describe la introducción de bibliotecas para Windows 7 y versiones posteriores. Las bibliotecas son una característica de Shell de Windows. Para tener acceso a la funcionalidad del shell de Windows, como las bibliotecas, los desarrolladores de otras aplicaciones de Windows Search deben implementar primero un almacén de datos de Shell. Para obtener más información, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Este tema se organiza de la siguiente manera:

- [Bibliotecas](#libraries)
  - [Puntos de entrada de datos de usuario](#user-data-entry-points)
  - [Colecciones de carpetas](#collections-of-folders)
  - [Carpetas admitidas en bibliotecas](#supported-folders-in-libraries)
  - [Copia de seguridad de almacenamiento](#storage-backed)
  - [Contenedores de Shell de sistema sin archivos](#non-file-system-shell-containers)
  - [Descripciones de biblioteca](#library-descriptions)
- [Temas relacionados](#related-topics)

## <a name="libraries"></a>Bibliotecas

En Windows 7 y versiones posteriores, las bibliotecas son el repositorio predeterminado de datos de usuario. Los usuarios pueden examinar los archivos del mismo modo que lo harían en una carpeta, o bien pueden ver sus archivos organizados por propiedades como fecha, tipo y autor. A diferencia de una carpeta, una biblioteca no almacena realmente elementos, pero muestra los archivos que se almacenan en varias carpetas al mismo tiempo. Las bibliotecas proporcionan un único punto de acceso y una vista enriquecida que dinamiza a los usuarios de su contenido agregado. Por ejemplo, si un usuario tiene archivos de música en carpetas de una unidad externa además de la carpeta **mi música** , puede tener acceso inmediato a todos los archivos de música a través de la biblioteca de música.

### <a name="user-data-entry-points"></a>Puntos de entrada de datos de usuario

Las bibliotecas predeterminadas (como **Mis documentos**, **Mis imágenes**, etc.) son el equivalente de la [carpeta conocida](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). Las bibliotecas predeterminadas proporcionan puntos de entrada conocidos a los usuarios, pero como el contenido de la biblioteca no está limitado a las bibliotecas de contenido de carpetas conocidas, los usuarios tienen más libertad para determinar dónde deben almacenarse los documentos y los medios. Las bibliotecas se exponen a través del espacio de nombres del shell (origen de datos del shell). La aplicación puede proporcionar a los usuarios los mismos puntos de entrada conocidos para sus datos mediante la habilitación del reconocimiento de la biblioteca y la exploración.

### <a name="collections-of-folders"></a>Colecciones de carpetas

Las bibliotecas son colecciones de contenido definidas por el usuario. Windows Search indexa las carpetas admitidas cuando se incluyen en las bibliotecas. Esto habilita la búsqueda instantánea y las vistas de disposición de pila basadas en propiedades en las bibliotecas.

### <a name="supported-folders-in-libraries"></a>Carpetas admitidas en bibliotecas

En el caso de las carpetas que se van a admitir en las bibliotecas, deben indexarse en el equipo local e indexarse en un equipo Windows remoto, o bien indizarse en un servidor con archivos indizados por Windows Search.

Los usuarios no pueden agregar carpetas no compatibles en el cuadro de diálogo de administración de la biblioteca de Windows. Si se agregan carpetas remotas no indizadas a una biblioteca mediante la API de [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) , la experiencia del usuario de la biblioteca volverá al **modo seguro** de la biblioteca. En **modo seguro** , se quitan de la biblioteca afectada características como las vistas de organización de la pila basada en propiedades, las sugerencias de filtro y la compatibilidad con la búsqueda del **menú Inicio** .

En la tabla siguiente se enumeran las carpetas incluidas en las bibliotecas mediante el cuadro de diálogo Administración de la biblioteca del explorador de Windows y las carpetas que no se admiten en **modo seguro**:

| Carpetas admitidas                                                                                                                            | Carpetas no compatibles                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Discos duros NTFS y FAT32 fijos y externos                                                                                                | Unidades extraíbles (como tarjetas thumbdrives y SD)                                                     |
| Recursos compartidos indexados por búsqueda de Windows (como servidores de departamento y en equipos que ejecutan Windows 10 y Windows 7 Home Edition) | Medios extraíbles (como CDs y DVDs)                                                                  |
| Recursos compartidos que están disponibles sin conexión (como **Mis documentos redirigidos**, **caché del lado cliente**)                                               | Recursos compartidos de red que no están disponibles sin conexión ni indexados de forma remota (como las unidades NAS)             |
| N/D                                                                                                                                          | Otros orígenes de datos (como Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive, etc.) |

### <a name="storage-backed"></a>Storage-Backed

Las bibliotecas son colecciones de carpetas de almacenamiento. Los usuarios pueden guardar y copiar archivos en una biblioteca directamente, ya que cada biblioteca tiene una ubicación de almacenamiento predeterminada a la que enviar estos archivos. En el caso de las bibliotecas predeterminadas, se trata de una carpeta conocida por el usuario que se incluye en una biblioteca (como **Mis documentos**) o la primera carpeta agregada a una biblioteca personalizada. Se trata de la carpeta donde los archivos salen cuando un usuario arrastra y coloca archivos en una biblioteca o guarda en una biblioteca con el cuadro de diálogo de archivo común. El usuario puede cambiar la ubicación de guardado predeterminada de una biblioteca en cualquier momento, pero si quita la ubicación de almacenamiento predeterminada, la siguiente carpeta de la biblioteca se seleccionará como la nueva ubicación de almacenamiento. Además, los usuarios pueden guardar en cualquier carpeta en la que tengan permisos que se hayan incluido en una biblioteca.

### <a name="non-file-system-shell-containers"></a>Contenedores de Shell de sistema sin archivos

Las bibliotecas pueden contener contenedores de Shell del sistema de archivos, como el **equipo** y el **Panel de control**, pero contienen elementos del sistema de archivos. Se pueden enumerar y obtener acceso a las carpetas y el contenido de la biblioteca mediante las API de archivos y carpetas del sistema de archivos en sistemas operativos anteriores. Si la aplicación depende en gran medida de las API específicas del sistema de archivos, se puede usar la API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para obtener las rutas de acceso del sistema de archivos de las carpetas y los archivos de las bibliotecas. En la mayoría de los casos, se recomienda usar el modelo de programación de Shell para admitir varias versiones de Windows y la flexibilidad de los elementos. Para obtener más información, vea [navegar por el espacio de nombres del shell](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Descripciones de biblioteca

Las descripciones de biblioteca se guardan en el disco como un archivo XML en la carpeta% appdata% Microsoft \\ Windows \\ Libraries (y posiblemente como **\_ bibliotecas FOLDERID**. Para obtener más información sobre las **\_ bibliotecas de FOLDERID**, consulte [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Los archivos de descripción de la biblioteca son archivos XML con la extensión de nombre de archivo. Library-ms. Las aplicaciones nunca deben tener acceso a los archivos ni editarlos. El texto de la ruta de acceso de la carpeta conservada en los archivos de descripción de la biblioteca no siempre es actual. Las carpetas de la biblioteca se guardan en el archivo de descripción de la biblioteca en el formato de [vínculos del shell](/windows/desktop/shell/links) binario serializado. Para obtener más información sobre las bibliotecas y el esquema de descripción de la biblioteca, vea [esquema de Descripción](../shell/library-schema-entry.md)de la biblioteca. Para obtener más información sobre los conectores de búsqueda federada y el esquema de Descripción del conector de búsqueda, [Busque el esquema de Descripción del conector](search-sconn-desc-schema-entry.md)de búsqueda.

> [NOTA]  
> Las aplicaciones siempre deben usar el modelo de programación de shell o la API de [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para consumir y manipular el contenido de la biblioteca, y no intentar tener acceso manualmente o editar el archivo de descripción de la biblioteca.

## <a name="related-topics"></a>Temas relacionados

[Búsqueda de Windows 7](./-search-3x-wds-overview.md)

[Novedades de Windows 7 Search](new-for-windows-7-search.md)

[Indexación de los eventos de priorización y de conjunto de filas en Windows 7](indexing-prioritization-and-rowset-events.md)