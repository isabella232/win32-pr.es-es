---
description: Cloud Filter API proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motores de sincronización en la nube
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718594"
---
# <a name="cloud-sync-engines"></a>Motores de sincronización en la nube

Vea también [ejemplo de reflejo en la nube](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).

A partir de Windows 10, versión 1709, Windows proporciona la *API de archivos* en la nube. Esta API está compuesta de varias API nativas de Win32 y WinRT que formalizan la compatibilidad con los motores de sincronización en la nube y administran tareas como la creación y administración de archivos y directorios de marcadores de posición. Los usuarios de esta API suelen ser proveedores de sincronización y, en cierto grado, aplicaciones Windows.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                | Descripción                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Compilar un motor de sincronización en la nube que admita archivos de marcadores de posición](build-a-cloud-file-sync-engine.md)<br/> | Aprenda a usar la API de archivos en la nube para crear un motor de sincronización de archivos en la nube que incluya archivos de marcadores de posición e integración con el explorador de archivos. <br/> |
| [Referencia de filtro de nube](cloud-filter-reference.md)<br/> | Cloud Filter API es una API nativa de Win32 que forma parte de la API de archivos en la nube más amplia. Cloud Filter API proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos. Esta API controla la creación y administración de archivos y directorios de marcadores de posición. <br/> |

