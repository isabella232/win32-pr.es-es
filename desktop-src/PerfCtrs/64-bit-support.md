---
description: Si proporciona contadores en un equipo de 64 bits, debe instalar la versión de 32 y 64 bits del proveedor en el equipo si desea admitir consumidores de 32 y 64 bits.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: Compatibilidad con 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e465529f35d8a9becb2583e9d5c00ac19a74d3be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062901"
---
# <a name="64-bit-support"></a>Compatibilidad con 64 bits

Un archivo DLL de proveedor de datos de rendimiento de 64 bits no se puede ejecutar en un proceso de consumidor de 32 bits y un archivo DLL de proveedor de datos de rendimiento de 32 bits no se puede ejecutar en un proceso de 64 bits. El registro del proveedor solo admite un valor único para la ruta de acceso a la DLL del proveedor de datos de rendimiento, por lo que no puede proporcionar rutas de acceso diferentes para que las usen consumidores de 32 bits y consumidores de `Library` 64 bits.

Las siguientes opciones están disponibles para admitir proveedores V1 en sistemas operativos de 64 bits:

- **Recomendado:** Instale y registre la ruta de acceso a la versión de 32 bits del archivo DLL del proveedor.
  - Los consumidores de 32 bits funcionarán de forma nativa: cargarán el archivo DLL del proveedor de 32 bits en el proceso de consumidor de 32 bits.
  - Los consumidores de 64 bits funcionarán indirectamente: no podrán cargar el archivo DLL del proveedor de 32 bits en el proceso de consumidor de 64 bits, pero Windows volverá automáticamente a crear un proceso de perfhost de 32 bits, cargará el archivo DLL del proveedor de 32 bits en el proceso de perfhost y enviará datos de rendimiento del proceso de perfhost de 32 bits al proceso de consumidor de 64 bits.
- **Solo 64 bits:** Instale y registre la ruta de acceso a la versión de 64 bits del archivo DLL del proveedor.
  - Se producirá un error en los consumidores de 32 bits: no podrán cargar el archivo DLL del proveedor de 64 bits en el proceso de 32 bits.
  - Los consumidores de 64 bits funcionarán de forma nativa: cargarán el archivo DLL del proveedor de 32 bits en proceso.

> [!NOTE]
> Varios proveedores de datos de rendimiento Windows integrados instalan un archivo DLL de 32 bits en , instalan un archivo DLL de 64 bits en y registran la ruta de acceso como , lo que permite que el redireccionamiento del sistema de archivos resuelva la ruta de acceso al archivo `%systemroot%\syswow64` `%systemroot%\system32` DLL `Library` `%systemroot%\system32\ProviderName.dll` adecuado. Esto solo se admite para los proveedores de datos de rendimiento que forman parte del Windows operativo. Los proveedores que no forman parte del Windows operativo no deben instalar archivos en la `Windows` carpeta . Los archivos no reconocidos de la carpeta se pueden `Windows` quitar durante el mantenimiento o la actualización.
