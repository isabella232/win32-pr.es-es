---
description: El servicio de seguimiento de vínculos distribuidos permite a las aplicaciones cliente realizar un seguimiento de los orígenes de vínculos que se han despasado.
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: Seguimiento de vínculos distribuidos e identificadores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d28e151c21fd5320a41950be7647c1e8e0a88b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105670211"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>Seguimiento de vínculos distribuidos e identificadores de objetos

Almacenar una referencia a un archivo o directorio mediante su ruta de acceso y el nombre de archivo no es confiable. Si un usuario cambia el nombre de un archivo, rompe los vínculos al archivo. Si un usuario cambia el nombre del directorio, rompe los vínculos al archivo y todos los archivos y subdirectorios en el árbol de directorios.

El **servicio de seguimiento de vínculos distribuidos** permite a las aplicaciones cliente realizar un seguimiento de los orígenes de vínculos que se han despasado. Los clientes que se suscriben al servicio de seguimiento de vínculos pueden mantener la integridad de sus referencias y se puede realizar un seguimiento de los objetos de forma transparente para el usuario.

## <a name="object-identifiers"></a>Identificadores de objetos

El servicio de seguimiento de vínculos mantiene su vínculo a un objeto mediante un **identificador de objeto (ID.)**. Un identificador de objeto es un atributo opcional que identifica de forma única un archivo o un directorio en un volumen.

Un índice de todos los identificadores de objeto se almacena en el volumen. Las operaciones de cambio de nombre, copia de seguridad y restauración conservan los identificadores de objeto. Sin embargo, las operaciones de copia no conservan los identificadores de objeto, ya que esto infringiría su unicidad.

Puede realizar las siguientes operaciones en los identificadores de objeto:

-   Creación
-   Eliminación
-   Consultar

Cuando se crea un identificador de objeto, se establece la identidad del archivo en el servicio de seguimiento de vínculos. Por el contrario, cuando se elimina un identificador de objeto, el servicio de seguimiento de vínculos deja de mantener vínculos al archivo. Para obtener una lista de los códigos de control del sistema de archivos que realizan operaciones en los identificadores de objeto, vea [códigos de control de administración de archivos](file-management-control-codes.md).

El servicio de seguimiento de vínculos distribuidos realiza un seguimiento de los orígenes de vínculo para los accesos directos de Shell y los vínculos OLE dentro de volúmenes del sistema de archivos NTFS El cliente de vínculo puede corregir un vínculo roto con información actualizada en la nueva ubicación del origen del vínculo.

## <a name="link-tracking-features"></a>Características de seguimiento de vínculos

Los métodos abreviados de Shell incluyen el seguimiento de vínculos heurísticos que usa un algoritmo de búsqueda de árbol para encontrar una coincidencia para un origen de vínculo que se ha pasado. El algoritmo de búsqueda se basa en la última ruta de acceso conocida de la información de archivo y archivo que incluye la fecha de creación, el tamaño de archivo y el nombre de archivo y la extensión.

La vinculación OLE incluye el mismo seguimiento de vínculos heurísticos. Windows también incluye el mismo seguimiento de vínculos heurísticos con algunas mejoras adicionales para buscar en los espacios de nombres para producir resultados en algunos escenarios comunes. Las mejoras incluyen el procedimiento siguiente, que depende de los límites de tiempo impuestos por una aplicación cliente.

**Para buscar espacios de nombres**

1.  Busque en cuatro niveles de directorio hacia abajo desde el último directorio.
2.  Suba un directorio y repita los pasos 1 y 2 otro tres veces, lo que puede producir resultados si el objeto se ha movido hacia abajo.
3.  Busque cuatro niveles por debajo de la raíz del escritorio, lo que puede producir resultados si el objeto se ha despasado a una ubicación en el mismo escritorio.
4.  Busque cuatro niveles por debajo de la raíz en cada unidad fija local.
5.  Repita los pasos 1-3 sin el límite de cuatro directorios.

> [!Note]  
> Estos esquemas de seguimiento de vínculos son transparentes para el usuario final. Sin embargo, no siempre generan resultados positivos y pueden llevar mucho tiempo.

 

Para obtener más información sobre los métodos abreviados de Shell, vea [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).

Para obtener más información acerca de los vínculos OLE, vea [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).

Si se realiza un vínculo a un archivo en NTFS 3,0 o posterior, y el archivo se mueve a cualquier otro volumen con NTFS 3,0 o posterior en el mismo dominio, el servicio de seguimiento puede encontrar el archivo, sujeto a consideraciones de tiempo. Además, si el archivo se mueve fuera del dominio o dentro de un grupo de trabajo, se encuentra.

Para obtener la versión NTFS de un volumen, abra un símbolo del sistema con derechos de acceso de administrador y ejecute el siguiente comando:

**fsutil fsinfo ntfsinfo** *X ** * *:*

donde *X* es la letra de la unidad del volumen.

Cuando se crea un vínculo a un archivo, el archivo de destino se considera el **origen del vínculo** y el creador del vínculo es el **cliente del vínculo**. Por ejemplo, si se crea un acceso directo de Shell para vincular a un documento de texto, el documento de texto es el origen del vínculo y el acceso directo del shell es el cliente del vínculo.

El servicio de seguimiento de vínculos distribuidos mantiene vínculos de archivos para las siguientes situaciones que se producen dentro de un dominio:

-   El archivo de origen del vínculo se mueve de un volumen del sistema de archivos NTFS a otro dentro del mismo dominio.
-   Se cambia el nombre del equipo que contiene el origen del vínculo.
-   Se cambian los recursos compartidos de red en el equipo de origen del vínculo.
-   El volumen que contiene el archivo de origen del vínculo se mueve a otro equipo del mismo dominio.

El servicio de seguimiento de vínculos distribuidos también intenta mantener vínculos en las situaciones anteriores incluso cuando no se producen dentro de un dominio, es decir, son entre dominios o dentro de un grupo de trabajo. Los vínculos siempre se pueden mantener en estas situaciones cuando se cambia el recurso compartido de red en el equipo de origen del vínculo. También se pueden mantener cuando un origen de vínculo se mueve dentro de un equipo. Normalmente, los vínculos se pueden mantener cuando el origen del vínculo se mueve a otro equipo, pero esta forma de seguimiento es menos confiable con el tiempo.

## <a name="link-tracking-functionality"></a>Funcionalidad de seguimiento de vínculos

La funcionalidad de seguimiento de vínculos se implementa principalmente en la forma de los dos servicios del sistema siguientes:

-   Cliente de seguimiento de vínculos distribuidos.
-   Servidor de seguimiento de vínculos distribuidos

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Cliente de seguimiento de vínculos distribuidos
</dt> <dd>

El cliente de seguimiento de vínculos distribuidos se ejecuta en todos los equipos y administra las actividades de seguimiento de vínculos para ese equipo. Estas actividades incluyen la búsqueda de orígenes de vínculo y el procesamiento de los movimientos de origen del vínculo. Cuando se mueve un origen de vínculo, el servicio pasa información al servidor de seguimiento de vínculos distribuido que se ejecuta en los controladores de dominio.

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Servidor de seguimiento de vínculos distribuidos
</dt> <dd>

El servidor de seguimiento de vínculos distribuido se ejecuta en cada controlador de dominio de un dominio. El servicio acepta las notificaciones de los movimientos de archivos y volúmenes del servicio de seguimiento en un equipo y permite que el cliente de seguimiento de vínculos distribuidos consulte la ubicación actual de un origen de vínculo.

Este servicio de servidor mantiene información en los controladores de dominio sobre los volúmenes y los archivos que se movieron. La información sobre los movimientos no puede aumentar más allá de un tamaño específico y se quita automáticamente si no es necesario.

</dd> </dl>

Las interfaces [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) y [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) exponen los servicios de seguimiento de vínculos. Por lo tanto, los métodos abreviados de shell lo usan. Cuando se llama al método [**IShellLink:: Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) y no se encuentra el archivo de referente, por ejemplo, cuando el usuario activa un acceso directo de Shell, se llama automáticamente al servicio de seguimiento para buscar el archivo. Del mismo modo, cuando la implementación de [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) no puede encontrar un archivo, por ejemplo, en su método [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) , llama automáticamente a en el servicio de seguimiento.

## <a name="link-tracking-limitations"></a>Limitaciones de seguimiento de vínculos

Los servicios de seguimiento de vínculos distribuidos solo están disponibles en el sistema de archivos NTFS y solo están disponibles para orígenes de vínculos en NTFS 3,0 o posterior. Por lo tanto, si se mueve un origen de vínculo a un volumen del sistema de archivos FAT, se pierde la información de seguimiento. Además, si un origen de vínculo se mueve entre NTFS 3,0 o posterior, pero el equipo que está realizando el traslado está ejecutando una versión anterior de Windows, se pierde la información de seguimiento de vínculos. Cuando se pierde la información de seguimiento de vínculos, no se produce ningún daño en el propio archivo de origen del vínculo, ya que los servicios de seguimiento de vínculos distribuidos no son de solo seguimiento.

Para obtener la versión NTFS de un volumen, abra un símbolo del sistema con derechos de acceso de administrador y ejecute el siguiente comando:

**fsutil fsinfo ntfsinfo** *X ** * *:*

donde *X* es la letra de la unidad del volumen.

Los vínculos a archivos en medios extraíbles no se mantienen. Además, el servicio de seguimiento no reconoce un nuevo volumen del sistema de archivos NTFS hasta que se reinicia el sistema. Un nuevo volumen podría estar disponible debido a una nueva creación de particiones, al volver a formatear un volumen del sistema de archivos FAT al sistema de archivos NTFS o al conectar una nueva unidad externa.

 

 
