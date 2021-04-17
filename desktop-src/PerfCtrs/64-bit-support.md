---
description: Si proporciona contadores en un equipo de 64 bits, debe instalar la versión de 32 bits y la de 64 bits del proveedor en el equipo si desea admitir consumidores de 32 y de 64 bits.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: Compatibilidad con 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e465529f35d8a9becb2583e9d5c00ac19a74d3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667357"
---
# <a name="64-bit-support"></a>Compatibilidad con 64 bits

Una DLL de proveedor de datos de rendimiento de 64 bits no se puede ejecutar en un proceso de consumidor de 32 bits y una DLL de proveedor de datos de rendimiento de 32 bits no se puede ejecutar en un proceso de 64 bits. El registro del proveedor solo admite un `Library` valor único para la ruta de acceso al archivo DLL del proveedor de datos de rendimiento, por lo que no puede proporcionar diferentes rutas de acceso para los consumidores de 32 bits y los consumidores de 64 bits.

Las siguientes opciones están disponibles para admitir los proveedores V1 en los sistemas operativos de 64 bits:

- **Recomendado:** Instale y registre la ruta de acceso a la versión de 32 bits de la DLL del proveedor.
  - los consumidores de 32 bits funcionarán de forma nativa: cargarán la DLL del proveedor de 32 bits en el proceso de consumidor de 32 bits.
  - los consumidores de 64 bits funcionarán de forma indirecta: no podrán cargar el archivo DLL de proveedor de 32 bits en el proceso de consumidor de 64 bits, pero Windows revertirá automáticamente a la creación de un proceso de perfhost de 32 bits, cargará la DLL del proveedor de 32 bits en el proceso de perfhost y enviará datos de rendimiento desde el proceso de perfhost de 32 bits al proceso de
- **solo 64 bits:** Instale y registre la ruta de acceso a la versión de 64 bits de la DLL del proveedor.
  - se producirá un error en los consumidores de 32 bits: no podrán cargar el archivo DLL de proveedor de 64 bits en el proceso de 32 bits.
  - los consumidores de 64 bits funcionarán de forma nativa: cargarán el archivo DLL de proveedor de 32 bits en proceso.

> [!NOTE]
> Varios proveedores de datos de rendimiento de Windows integrados instalan un archivo DLL de 32 bits en `%systemroot%\syswow64` , instalan un archivo dll de 64 bits en `%systemroot%\system32` y registran la `Library` ruta de acceso como `%systemroot%\system32\ProviderName.dll` , lo que permite que la redirección del sistema de archivos resuelva la ruta de acceso al archivo dll adecuado. Esto solo se admite para los proveedores de datos de rendimiento que forman parte del sistema operativo Windows. Los proveedores que no forman parte del sistema operativo Windows no deben instalar archivos en la `Windows` carpeta. Los archivos no reconocidos en la `Windows` carpeta se pueden quitar durante el mantenimiento o la actualización.
