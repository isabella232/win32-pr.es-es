---
description: Los proveedores administran volúmenes en ejecución y crean instantáneas de ellos a petición.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb336dbb51fcbd715ea236ecdc0c62d81daf29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696983"
---
# <a name="providers"></a>Proveedores

Los [*proveedores*](vssgloss-p.md) administran volúmenes en ejecución y crean instantáneas de ellos a petición.

En respuesta a una solicitud de un solicitante, un proveedor genera eventos COM para indicar a las aplicaciones de una instantánea próxima y, después, crea y mantiene esa copia hasta que ya no se necesita.

Mientras existe una instantánea, el proveedor crea un entorno en el que hay dos copias independientes de cualquier volumen del que se ha realizado una instantánea: uno de los discos en ejecución que se usa y se actualiza como normal, el otro que es el disco fijo y estable para la copia de seguridad.

Aunque se proporciona un proveedor predeterminado como parte de Windows, otros proveedores pueden proporcionar sus propias implementaciones que están optimizadas para sus propias ofertas de software y hardware de almacenamiento.

Desde el punto de vista de un usuario final o un desarrollador de aplicaciones de copia de seguridad o restauración, todos los proveedores tendrán la misma interfaz (consulte [selección de proveedores](selecting-providers.md)).

Todos los proveedores deben ser capaces de hacer lo siguiente:

-   Interceptar las solicitudes de e/s entre el sistema de archivos y el sistema de almacenamiento masivo subyacente.
-   Capture y recupere el estado de un volumen en el momento de la instantánea, manteniendo una vista "a un momento dado" de los archivos en el disco sin operaciones de e/s parciales reflejadas en su estado.
-   Use esta vista de "momento dado" para exponer (como mínimo, las aplicaciones habilitadas para VSS) un volumen virtual que contenga los datos de la instantánea.

En función de cómo se realice, un proveedor puede ser de uno de estos tres tipos:

-   [Proveedor del sistema](#system-provider)
-   [Proveedores de software](#software-providers)
-   [Proveedores de hardware](#hardware-providers)

## <a name="system-provider"></a>Proveedor del sistema

Un proveedor de instantáneas, el [*proveedor del sistema*](vssgloss-s.md), se proporciona como parte predeterminada de una instalación del sistema operativo Windows. Actualmente, el proveedor del sistema es una instancia concreta de un proveedor de software. Sin embargo, esto puede cambiar en el futuro.

Para mantener una vista "a un momento dado" de un volumen incluido en la instantánea, el proveedor del sistema utiliza una técnica de copia en escritura. Las copias de los sectores del disco que se han modificado (denominadas "diferencias") desde el inicio de la creación de instantáneas se almacenan en un área de almacenamiento de instantáneas.

Por lo tanto, el proveedor del sistema puede exponer el volumen activo, que se puede escribir y leer de forma normal, y aplicar las "diferencias" a los datos del volumen activo para exponer eficazmente los datos inmovilizados de la instantánea.

En el caso del proveedor del sistema, el área de almacenamiento de instantáneas debe encontrarse en un volumen NTFS. No es necesario que el volumen del que se va a realizar la instantánea sea un volumen NTFS, pero al menos un volumen montado en el sistema debe ser de este tipo.

## <a name="software-providers"></a>Proveedores de software

Los proveedores de instantáneas de software interceptan y procesan solicitudes de e/s en una capa de software entre el sistema de archivos y el software de Volume Manager. Estos proveedores se implementan como un componente DLL de modo usuario y al menos un controlador de dispositivo de modo kernel, normalmente (pero no necesariamente) un controlador de filtro de almacenamiento. El trabajo de creación de estas instantáneas se realiza en el software.

Un proveedor de instantáneas de software debe mantener una vista "a un momento dado" de un volumen mediante el acceso a un conjunto de archivos que se pueden usar para volver a crear con precisión el estado del volumen antes de la instantánea. Un ejemplo de esto es la técnica de copia en escritura del proveedor del sistema.

Sin embargo, VSS no impone ninguna restricción sobre la técnica que usan los proveedores de software para crear y mantener instantáneas, y los proveedores de terceros pueden implementar sus proveedores de software tal y como se ven.

Además, VSS proporciona compatibilidad con gran parte de la funcionalidad de los proveedores de instantáneas de software, como la definición de un momento dado, la sincronización y el vaciado de datos, proporcionando una interfaz común para las aplicaciones de copia de seguridad y la administración de la instantánea.

Por definición, un proveedor de software se puede aplicar a una gama más amplia de plataformas de almacenamiento que a un proveedor de hardware, y debe poder trabajar con discos básicos o volúmenes lógicos igualmente bien. Esta generalidad sacrifica el rendimiento que puede estar disponible mediante la implementación de instantáneas en hardware y no hace uso de las características de captura de volumen o de creación de reflejo de archivos específicas del proveedor.

## <a name="hardware-providers"></a>Proveedores de hardware

Los proveedores de instantáneas de hardware interceptan las solicitudes de e/s del sistema de archivos en el nivel de hardware al trabajar junto con un controlador o adaptador de almacenamiento de hardware. El trabajo de creación de la instantánea se realiza mediante un adaptador de host, un dispositivo de almacenamiento o una controladora RAID fuera del sistema operativo.

Estos proveedores se implementan como un componente DLL de modo usuario que se comunica con el hardware que expondrá los datos de la instantánea: por lo tanto, los proveedores de instantáneas de hardware pueden necesitar llamar o crear otros componentes en modo kernel.

Los proveedores de hardware exponen a las instantáneas de VSS de discos completos o unidades lógicas (LUN). Los solicitantes todavía tratan las instantáneas de los volúmenes; VSS controla internamente todas las asignaciones de volumen a disco. Las instantáneas creadas por proveedores de hardware de volúmenes que residen en discos dinámicos tienen un requisito específico: no se pueden importar en el mismo sistema. Deben crearse y exportarse en un segundo sistema.

Mientras que un proveedor de instantáneas de hardware hace uso de la funcionalidad de VSS que define el momento dado, permite la sincronización de datos, administra la instantánea y proporciona una interfaz común con las aplicaciones de copia de seguridad, VSS no especifica el mecanismo subyacente por el que el proveedor de hardware genera y mantiene instantáneas.

 

 



