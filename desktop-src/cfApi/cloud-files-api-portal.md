---
description: Cloud Filter API proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motores de sincronización en la nube
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549600"
---
# <a name="cloud-sync-engines"></a>Motores de sincronización en la nube

Consulte también ejemplo [de Cloud Mirror.](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)

A partir Windows 10, versión 1709, Windows proporciona la *API de archivos en la nube*. Esta API consta de varias API nativas de Win32 y WinRT que formalizan la compatibilidad con los motores de sincronización en la nube y controla tareas como la creación y administración de archivos y directorios de marcadores de posición. Los usuarios de esta API suelen ser proveedores de sincronización y, en cierta medida, aplicaciones de Windows.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                | Descripción                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Compilación de un motor de sincronización en la nube que admita archivos de marcador de posición](build-a-cloud-file-sync-engine.md)<br/> | Aprenda a usar la API de archivos en la nube para crear un motor de sincronización de archivos en la nube que incluya archivos de marcador de posición Explorador de archivos integración. <br/> |
| [Referencia de filtro de nube](cloud-filter-reference.md)<br/> | La API de filtro de nube es una API nativa de Win32 que forma parte de la API de archivos en la nube más amplia. La API de filtro de nube proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos. Esta API controla la creación y administración de directorios y archivos de marcador de posición. <br/> |