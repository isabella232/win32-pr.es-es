---
title: Windows Sistema de archivos proyectado
description: Información general sobre el Windows de archivos proyectados (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: d5cb20b123e72ec8e031036019a16ef1bbe2b8dc4b9bb53446c8faaced4d796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792662"
---
# <a name="windows-projected-file-system-projfs"></a>Windows Sistema de archivos proyectado (ProjFS)

El Windows Projected File System (ProjFS) permite que una aplicación en modo de usuario denominada "proveedor" proyecte datos jerárquicos de un almacén de datos de respaldo en el sistema de archivos, lo que hace que aparezcan como archivos y directorios en el sistema de archivos. Por ejemplo, un proveedor simple podría proyectar el registro Windows en el sistema de archivos, lo que hace que las claves y los valores del Registro aparezcan como archivos y directorios, respectivamente. Un ejemplo de un proveedor más complejo es [VFS para Git,](https://github.com/Microsoft/VFSForGit)que se usa para virtualizar repositorios de Git muy grandes.

> [!NOTE]
> ProjFS está diseñado para su uso con almacenes de datos de respaldo de alta velocidad. Uno de sus objetivos de diseño es hacer que los datos proyectados aparezcan como si estuvieran presentes localmente, ocultando el hecho de que los datos pueden ser remotos. Por lo tanto, ProjFS no proporciona: mecanismos para notificar el progreso de la recuperación de datos; indicación del estado en línea frente al estado sin conexión de un archivo; ni otras características que puedan ser deseables al trabajar con almacenes de datos de respaldo que son lentos. Para estos escenarios, considere la posibilidad de usar cloud files API en [su lugar.](../cfapi/cloud-files-api-portal.md)

## <a name="in-this-section"></a>En esta sección

| Tema                                                                                                       | Descripción |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Guía de programación del sistema de archivos proyectado](projfs-programming-guide.md)                              | Información conceptual sobre la implementación de una aplicación de proveedor ProjFS.
| [Windows Referencia de API del sistema de archivos proyectado](projfs-reference.md)                                          | Información de referencia para la interfaz de programación ProjFS.
| [Windows Glosario del sistema de archivos proyectado](projfs-glossary.md)                                                | Términos especiales usados en ProjFS.

## <a name="additional-resources"></a>Recursos adicionales

| Tema                                                                                                             | Descripción                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Ejemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Proveedor ProjFS de ejemplo que proyecta el Windows en el sistema de archivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->