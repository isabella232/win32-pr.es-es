---
title: Sistema de archivos previsto de Windows
description: Información general sobre el sistema de archivos previsto para Windows (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 8391ec63f23c9ebae5b47e4cac862f6ab3079ceb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904645"
---
# <a name="windows-projected-file-system-projfs"></a>Sistema de archivos previsto para Windows (ProjFS)

El sistema de archivos previsto para Windows (ProjFS) permite que una aplicación de modo de usuario denominada "proveedor" proyecte los datos jerárquicos de un almacén de datos de respaldo en el sistema de archivos, de forma que aparezcan como archivos y directorios en el sistema de archivos. Por ejemplo, un proveedor simple podría proyectar el registro de Windows en el sistema de archivos, por lo que las claves y los valores del registro aparecen como archivos y directorios, respectivamente. Un ejemplo de un proveedor más complejo es [VFS para git](https://github.com/Microsoft/VFSForGit), que se usa para virtualizar repositorioss de Git de gran tamaño.

> [!NOTE]
> ProjFS está diseñado para su uso con almacenes de datos de respaldo de alta velocidad. Uno de sus objetivos de diseño es hacer que los datos proyectados aparezcan como si estuviesen presentes localmente, ocultando el hecho de que los datos pueden ser remotos. Como tal, ProjFS no proporciona: mecanismos para notificar el progreso de la recuperación de datos; indicación del estado en línea frente a sin conexión de un archivo; y otras características que pueden ser deseables al trabajar con almacenes de datos de respaldo que son lentos. En estos escenarios, considere la posibilidad de usar la [API de archivos](../cfapi/cloud-files-api-portal.md)en la nube.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                                                       | Descripción |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Guía de programación del sistema de archivos previsto en Windows](projfs-programming-guide.md)                              | Información conceptual sobre la implementación de una aplicación de proveedor de ProjFS.
| [Referencia de la API del sistema de archivos previsto de Windows](projfs-reference.md)                                          | Información de referencia de la interfaz de programación de ProjFS.
| [Glosario del sistema de archivos previsto de Windows](projfs-glossary.md)                                                | Términos especiales usados en ProjFS.

## <a name="additional-resources"></a>Recursos adicionales

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Ejemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Un proveedor de ProjFS de ejemplo que proyecta el registro de Windows en el sistema de archivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->