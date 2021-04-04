---
title: Guía de programación del sistema de archivos proyectado
description: Información conceptual sobre la implementación de una aplicación de proveedor de ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: a6b2d186ac3e674c3fa68e17ecd523b2c94f2401
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078069"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guía de programación del sistema de archivos proyectado (ProjFS)

El sistema de archivos previsto de Windows (ProjFS) permite que una aplicación de modo de usuario denominada "proveedor" proyecte los datos jerárquicos en el sistema de archivos, por lo que aparece como archivos y directorios en el sistema de archivos.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                                                       | Descripción |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Información general del proveedor](provider-overview.md)                                                                   | Información general conceptual de una aplicación de proveedor.
| [Estado de caché en la raíz de virtualización](cache-state.md)                                                    | Describe los distintos Estados de la memoria caché que puede tener un archivo o directorio administrado por el proveedor. 
| [Habilitación del sistema de archivos previsto de Windows](enabling-windows-projected-file-system.md)                         | Describe cómo habilitar el componente opcional ProjFS.
| [Ciclo de vida de la instancia de virtualización](virtualization-instance-lifecycle.md)                                   | Información general sobre el ciclo de vida de una instancia de virtualización de ProjFS.
| [Enumeración de archivos y directorios](enumerating-files-and-directories.md)                                   | Describe el modo en que un proveedor ProjFS participa en la enumeración de directorios.
| [Aprovisionamiento de datos de archivo](providing-file-data.md)                                                               | Describe cómo un proveedor suministra información de marcadores de posición y datos de archivos.
| [Notificaciones de operación del sistema de archivos](file-system-operation-notifications.md)                               | Describe cómo un proveedor puede recibir notificaciones de las operaciones del sistema de archivos.
| [Control de cambios de vista](handling-view-changes.md)                                                           | Describe cómo actualizar la vista de cliente de la memoria auxiliar de un proveedor.
| [Control asincrónico de devolución de llamada](asynchronous-callback-handling.md)                                         | Describe cómo el proveedor puede atender las devoluciones de llamada de forma asincrónica.
| [Referencia de la API del sistema de archivos previsto de Windows](/windows/desktop/api/_projfs) | Información de referencia de la interfaz de programación de ProjFS.

## <a name="additional-resources"></a>Recursos adicionales

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Ejemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Un proveedor de ProjFS de ejemplo que proyecta el registro de Windows en el sistema de archivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->