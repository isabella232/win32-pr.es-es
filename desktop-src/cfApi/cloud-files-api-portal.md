---
description: Cloud Filter API proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motores de Sincronización en la nube
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: 39dd28779c07dfd6e44fde0e53f583e72971d5883205f42581e3b5ac4102c0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551379"
---
# <a name="cloud-sync-engines"></a>Motores de Sincronización en la nube

Consulte también el [ejemplo de Reflejo de la nube](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).

A partir Windows 10, versión 1709, Windows proporciona la *API de archivos en la nube*. Esta API consta de varias API nativas de Win32 y WinRT que formalizan la compatibilidad con los motores de sincronización en la nube, y controla tareas como la creación y administración de directorios y archivos de marcador de posición. Los usuarios de esta API suelen ser proveedores de sincronización y, en cierta medida, Windows aplicaciones.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                | Descripción                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Compilación de un motor de Sincronización en la nube que admita archivos de marcador de posición](build-a-cloud-file-sync-engine.md)<br/> | Aprenda a usar la API de archivos en la nube para crear un motor de sincronización de archivos en la nube que incluya archivos de marcador de posición Explorador de archivos integración. <br/> |
| [Referencia de filtro de nube](cloud-filter-reference.md)<br/> | La API de filtro de nube es una API win32 nativa que forma parte de la API de archivos en la nube más amplia. La API de filtro de nube proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos. Esta API controla la creación y administración de directorios y archivos de marcador de posición. <br/> |