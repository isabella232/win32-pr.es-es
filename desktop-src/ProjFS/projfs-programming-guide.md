---
title: Guía de programación del sistema de archivos proyectado
description: Información conceptual sobre la implementación de una aplicación de proveedor ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 86c6f49eaf9da578226031eaf84abff7ebb059c0
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120570"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guía de programación del sistema de archivos proyectados (ProjFS)

El sistema de archivos proyectado de Windows (ProjFS) permite que una aplicación en modo de usuario denominada "proveedor" proyecte datos jerárquicos en el sistema de archivos, lo que hace que aparezcan como archivos y directorios en el sistema de archivos.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                                                       | Descripción |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Introducción al proveedor](provider-overview.md)                                                                   | Información general conceptual de una aplicación de proveedor.
| [Estado de caché en la raíz de virtualización](cache-state.md)                                                    | Describe los distintos estados de caché que puede tener un archivo o directorio administrado por el proveedor. 
| [Habilitación del sistema de archivos proyectado de Windows](enabling-windows-projected-file-system.md)                         | Describe cómo habilitar el componente opcional ProjFS.
| [Ciclo de vida de la instancia de virtualización](virtualization-instance-lifecycle.md)                                   | Información general sobre el ciclo de vida de una instancia de virtualización de ProjFS.
| [Enumeración de archivos y directorios](enumerating-files-and-directories.md)                                   | Describe cómo un proveedor ProjFS participa en la enumeración de directorios.
| [Aprovisionamiento de datos de archivo](providing-file-data.md)                                                               | Describe cómo un proveedor proporciona información de marcador de posición y datos de archivo.
| [Notificaciones de operación del sistema de archivos](file-system-operation-notifications.md)                               | Describe cómo un proveedor puede recibir notificaciones de operaciones del sistema de archivos.
| [Control de cambios en la vista](handling-view-changes.md)                                                           | Describe cómo actualizar la vista de cliente del almacén de respaldo de un proveedor.
| [Control asincrónico de devolución de llamada](asynchronous-callback-handling.md)                                         | Describe cómo el proveedor puede realizar devoluciones de llamada de servicio de forma asincrónica.
| [Referencia de la API del sistema de archivos proyectado de Windows](/windows/desktop/api/_projfs) | Información de referencia de la interfaz de programación ProjFS.

## <a name="additional-resources"></a>Recursos adicionales

| Tema                                                                                                             | Descripción                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Ejemplo regFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Un proveedor ProjFS de ejemplo que proyecta el Registro de Windows en el sistema de archivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->