---
description: Los proveedores administran volúmenes en ejecución y crean las instantáneas de ellos a petición.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9e098981c6246392fef75f717b1d7676df1aa134e4faef3e436ee8b3eb537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591332"
---
# <a name="providers"></a>Proveedores

[*Los proveedores*](vssgloss-p.md) administran volúmenes en ejecución y crean las instantáneas de ellos a petición.

En respuesta a una solicitud de un solicitante, un proveedor genera eventos COM para señalar las aplicaciones de una instantánea próxima y, a continuación, crea y mantiene esa copia hasta que ya no es necesaria.

Mientras existe una instantánea, el proveedor crea un entorno en el que hay efectivamente dos copias independientes de cualquier volumen que se ha copiado en la sombra: uno el disco en ejecución que se usa y actualiza de forma normal, el otro una copia fija y estable para la copia de seguridad.

Aunque se proporciona un proveedor predeterminado como parte de Windows, otros proveedores pueden proporcionar sus propias implementaciones que están optimizadas para sus propias ofertas de hardware y software de almacenamiento.

Desde el punto de vista de un usuario final o un desarrollador de aplicaciones de copia de seguridad o restauración, todos los proveedores tendrán la misma interfaz (consulte [Selección de proveedores).](selecting-providers.md)

Todos los proveedores deben poder hacer lo siguiente:

-   Interceptar solicitudes de E/S entre el sistema de archivos y el sistema de almacenamiento masivo subyacente.
-   Capture y recupere el estado de un volumen en el momento de la instantánea, manteniendo una vista "a un momento dado" de los archivos en el disco sin operaciones de E/S parciales reflejadas en su estado.
-   Use esta vista "a un momento dado" para exponer (mínimamente en aplicaciones habilitadas para VSS) un volumen virtual que contenga los datos copiados en la sombra.

En función de cómo se haga esto, un proveedor puede ser uno de estos tres tipos:

-   [Proveedor del sistema](#system-provider)
-   [Proveedores de software](#software-providers)
-   [Proveedores de hardware](#hardware-providers)

## <a name="system-provider"></a>Proveedor del sistema

Un proveedor de instantáneas, [*el proveedor del*](vssgloss-s.md)sistema , se proporciona como parte predeterminada de una Windows sistema operativo. Actualmente, el proveedor del sistema es una instancia determinada de un proveedor de software. Sin embargo, esto puede cambiar en el futuro.

Para mantener una vista "a un momento dado" de un volumen contenido en la instantánea, el proveedor del sistema usa una técnica de copia en escritura. Las copias de los sectores en disco que se han modificado (denominados "diferencias") desde el principio de la creación de instantáneas se almacenan en un área de almacenamiento de instantáneas.

Por lo tanto, el proveedor del sistema puede exponer el volumen en directo, que se puede escribir y leer con normalidad, y aplicar las "diferencias" a los datos del volumen en directo para exponer eficazmente los datos inmovilizados de la instantánea.

En el caso del proveedor del sistema, el área de almacenamiento de instantáneas debe encontrarse en un volumen NTFS. No es necesario que el volumen del que se va a realizar la instantánea sea un volumen NTFS, pero al menos un volumen montado en el sistema debe ser de este tipo.

## <a name="software-providers"></a>Proveedores de software

Los proveedores de instantáneas de software interceptan y procesan las solicitudes de E/S en una capa de software entre el sistema de archivos y el software del administrador de volúmenes. Estos proveedores se implementan como un componente DLL en modo de usuario y al menos un controlador de dispositivo en modo kernel, normalmente (pero no necesariamente) un controlador de filtro de almacenamiento. El trabajo de crear estas instantáneas se realiza en software.

Un proveedor de instantáneas de software debe mantener una vista "a un momento dado" de un volumen al tener acceso a un conjunto de archivos que se pueden usar para volver a crear con precisión el estado del volumen antes de la instantánea. Un ejemplo de esto es la técnica de copia en escritura del proveedor del sistema.

Sin embargo, VSS no aplica restricciones a la técnica que usan los proveedores de software para crear y mantener instantáneas, y los proveedores de terceros pueden implementar sus proveedores de software como les parezca oportuno.

Además, VSS proporciona compatibilidad con gran parte de la funcionalidad de los proveedores de instantáneas de software, como definir el momento dado, la sincronización y el vaciado de datos, proporcionar una interfaz común para las aplicaciones de copia de seguridad y la administración de la instantánea.

Por definición, un proveedor de software será aplicable a una gama más amplia de plataformas de almacenamiento que un proveedor de hardware y debería poder trabajar con discos básicos o volúmenes lógicos igualmente bien. Esta generalidad sacra el rendimiento que puede estar disponible mediante la implementación de instantáneas en hardware y no hace uso de ninguna captura de volumen específica del proveedor o características de creación de reflejo de archivos.

## <a name="hardware-providers"></a>Proveedores de hardware

Los proveedores de instantáneas de hardware interceptan las solicitudes de E/S del sistema de archivos en el nivel de hardware trabajando junto con un controlador o adaptador de almacenamiento de hardware. El trabajo de creación de la instantánea lo realiza un adaptador de host, un dispositivo de almacenamiento o un controlador RAID fuera del sistema operativo.

Estos proveedores se implementan como un componente DLL en modo de usuario que se comunica con el hardware que expondrá los datos de instantáneas: por lo tanto, es posible que los proveedores de instantáneas de hardware necesiten llamar o crear otros componentes en modo kernel.

Los proveedores de hardware exponen a instantáneas de VSS de discos o unidades lógicas (LUN) completos. Los solicitantes siguen trabajando con instantáneas de volúmenes. VSS controla internamente toda la asignación de volumen a disco. Las instantáneas creadas por proveedores de hardware de volúmenes que residen en discos dinámicos tienen un requisito específico: no se pueden importar en el mismo sistema. Deben crearse transportables e importarse en un segundo sistema.

Aunque un proveedor de instantáneas de hardware usa la funcionalidad de VSS que define el momento dado, permite la sincronización de datos, administra la instantánea y proporciona una interfaz común con las aplicaciones de copia de seguridad, VSS no especifica el mecanismo subyacente por el que el proveedor de hardware genera y mantiene instantáneas.

 

 



