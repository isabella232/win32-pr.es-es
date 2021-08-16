---
description: Describe la introducción de las bibliotecas para Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Windows Bibliotecas de shell en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f120f1bc4e4208a7e6bbf35bbcfc4717ed05dfb7344658a80b1ea1d9a3ba50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969604"
---
# <a name="windows-shell-libraries-in-windows"></a>Windows Bibliotecas de shell en Windows

En este tema se describe la introducción de las bibliotecas para Windows 7 y versiones posteriores. Las bibliotecas son una Windows Shell. Para acceder a Windows Shell, como bibliotecas, los desarrolladores de Windows Search deben implementar primero un almacén de datos de Shell. Para obtener más información, vea [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Este tema se organiza de la siguiente manera:

- [Bibliotecas](#libraries)
  - [Puntos de entrada de datos de usuario](#user-data-entry-points)
  - [Colecciones de carpetas](#collections-of-folders)
  - [Carpetas admitidas en bibliotecas](#supported-folders-in-libraries)
  - [Storage con copia de seguridad](#storage-backed)
  - [Contenedores de Shell del sistema que no son de archivos](#non-file-system-shell-containers)
  - [Descripciones de biblioteca](#library-descriptions)
- [Temas relacionados](#related-topics)

## <a name="libraries"></a>Bibliotecas

En Windows 7 y versiones posteriores, las bibliotecas son el repositorio predeterminado de datos de usuario. Los usuarios pueden examinar sus archivos de la misma manera que lo harían en una carpeta, o pueden ver sus archivos organizados por propiedades como fecha, tipo y autor. A diferencia de una carpeta, una biblioteca no almacena realmente elementos, pero muestra los archivos almacenados en varias carpetas al mismo tiempo. Las bibliotecas proporcionan un único punto de acceso y vistas enriquecciones dinámicas a los usuarios de su contenido agregado. Por ejemplo, si un usuario tiene archivos de música en carpetas de una unidad externa además de la carpeta Mi **Música,** puede acceder inmediatamente a todos los archivos de música a través de la biblioteca Música.

### <a name="user-data-entry-points"></a>Puntos de entrada de datos de usuario

Las bibliotecas predeterminadas **(como Mis documentos**, **Mis imágenes,** etc.) son equivalentes a [carpeta conocida.](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) Las bibliotecas predeterminadas proporcionan puntos de entrada conocidos a los usuarios, pero como el contenido de la biblioteca no se limita a las bibliotecas de contenido de carpetas conocidas, los usuarios tienen más libertad para determinar dónde se deben almacenar los documentos y los medios. Las bibliotecas se exponen a través del espacio de nombres shell (origen de datos de Shell). La aplicación puede proporcionar a los usuarios los mismos puntos de entrada conocidos a sus datos mediante la habilitación del reconocimiento de la biblioteca y la exploración.

### <a name="collections-of-folders"></a>Colecciones de carpetas

Las bibliotecas son colecciones de contenido definidas por el usuario. Windows Buscar en carpetas admitidas de índices cuando se incluyen en bibliotecas. Esto permite la búsqueda instantánea y las vistas de organización de pila basadas en propiedades en las bibliotecas.

### <a name="supported-folders-in-libraries"></a>Carpetas admitidas en bibliotecas

Para que las carpetas sean compatibles con las bibliotecas, deben ser indexables en el equipo local e indexadas en una máquina Windows remota o indexadas en un servidor con archivos indexados por Windows Search.

Los usuarios no pueden agregar carpetas no admitidas en el cuadro de diálogo Windows administración de bibliotecas. Si se agregan carpetas remotas no indexadas a una biblioteca mediante la API [IShellLibrary,](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) la experiencia del usuario de la biblioteca revertirá al modo Caja fuerte **biblioteca.** En **Caja fuerte modo** de inicio, como las vistas de organización  de pila basadas en propiedades, las sugerencias de filtro y la compatibilidad con la búsqueda del menú Inicio se quitan de la biblioteca afectada.

En la tabla siguiente se enumeran las carpetas incluidas en las bibliotecas mediante el cuadro de diálogo de administración de bibliotecas Windows Explorer y las carpetas que no se admiten **en Caja fuerte modo :**

| Carpetas admitidas                                                                                                                            | Carpetas no admitidas                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unidades de disco duro NTFS y FAT32 fijas y externas                                                                                                | Unidades extraíbles (como thumbdrives y tarjetas SD)                                                     |
| Recursos compartidos indexados por Windows Search (por ejemplo, servidores de departamento y en equipos que ejecutan Windows 10 y Windows edición 7 Home) | Medios extraíbles (como CD y DVD)                                                                  |
| Recursos compartidos que están disponibles sin conexión (como **Redirected Mis documentos**, Client **Side Cache**)                                               | Recursos compartidos de red que no están disponibles sin conexión ni indexados de forma remota (como unidades NAS)             |
| N/D                                                                                                                                          | Otros orígenes de datos (como Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive, etc.) |

### <a name="storage-backed"></a>Storage-Backed

Las bibliotecas son colecciones de carpetas de almacenamiento. Los usuarios pueden guardar y copiar archivos en una biblioteca directamente, ya que cada biblioteca tiene una ubicación de guardado predeterminada a la que enviar estos archivos. En el caso de las bibliotecas predeterminadas, se trata de la carpeta conocida del usuario que se incluye en una biblioteca (como **Mis documentos**) o la primera carpeta agregada a una biblioteca personalizada. Esta es la carpeta donde van los archivos cuando un usuario arrastra y coloca archivos en una biblioteca o se guarda en una biblioteca con el cuadro de diálogo de archivo común. El usuario puede cambiar la ubicación de guardado predeterminada de una biblioteca en cualquier momento, pero si quita la ubicación de guardado predeterminada, la carpeta siguiente de la biblioteca se seleccionará como la nueva ubicación de guardado. Los usuarios también pueden guardar en cualquier carpeta en la que tengan permisos que se haya incluido en una biblioteca.

### <a name="non-file-system-shell-containers"></a>Contenedores de Shell del sistema que no son de archivos

Las bibliotecas pueden contener contenedores de Shell del sistema de archivos, como **Equipo** **y Panel de control**, pero contienen elementos del sistema de archivos. Las carpetas y el contenido de la biblioteca se pueden enumerar y acceder a través de las API para archivos y carpetas del sistema de archivos en sistemas operativos anteriores. Si la aplicación depende en gran medida de las API específicas del sistema de archivos, la API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) se puede usar para obtener las rutas de acceso del sistema de archivos de carpetas y archivos dentro de las bibliotecas. En la mayoría de los casos, se recomienda usar el modelo de programación de Shell para admitir varias versiones Windows y flexibilidad de elementos. Para obtener más información, vea [Navegar por el espacio de nombres del shell](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Descripciones de biblioteca

Las descripciones de la biblioteca se guardan en el disco como un archivo XML en la carpeta %appdata%Microsoft Windows Libraries (y potencialmente como \\ \\ **\_ bibliotecas FOLDERID).** Para obtener más información sobre **las \_ bibliotecas FOLDERID**, vea [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Los archivos de descripción de biblioteca son archivos XML con la extensión de nombre de archivo .library-ms. Las aplicaciones nunca deben tener acceso a los archivos ni editarlos. El texto de la ruta de acceso de la carpeta persistente en los archivos de descripción de la biblioteca no siempre es actual. Las carpetas de biblioteca se conservan en el archivo de descripción de la biblioteca en el formato de vínculos [binarios de shell serializados.](/windows/desktop/shell/links) Para obtener más información sobre las bibliotecas y el esquema de descripción de la biblioteca, vea [Esquema de descripción de la biblioteca](../shell/library-schema-entry.md). Para obtener más información sobre los conectores de búsqueda federados y el esquema de descripción del conector de búsqueda, [esquema de descripción del conector de búsqueda](search-sconn-desc-schema-entry.md).

> [NOTA]  
> Las aplicaciones siempre deben usar el modelo de programación de Shell o la API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para consumir y manipular el contenido de la biblioteca, y no intentar acceder manualmente ni editar el archivo de descripción de la biblioteca.

## <a name="related-topics"></a>Temas relacionados

[Windows 7 Search](./-search-3x-wds-overview.md)

[Novedades de Windows 7 Search](new-for-windows-7-search.md)

[Indexación de eventos de priorización y conjunto de filas en Windows 7](indexing-prioritization-and-rowset-events.md)