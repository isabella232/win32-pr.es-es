---
description: Funciones que se usan para administrar carpetas montadas.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funciones de carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360815"
---
# <a name="mounted-folder-functions"></a>Funciones de carpeta montada

Las funciones de carpeta montada se pueden dividir en tres grupos: funciones de uso general, funciones usadas para buscar volúmenes y funciones que se usan para examinar un volumen en busca de carpetas montadas.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose funciones de carpeta montada



| Función                                                                     | Descripción                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Elimina una letra de unidad o una carpeta montada.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Recupera la ruta de acceso de GUID de volumen para el volumen asociado al punto de montaje de volumen especificado (letra de unidad, ruta de acceso de GUID de volumen o carpeta montada). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Recupera la carpeta montada que está asociada con el volumen especificado.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Asocia un volumen con una letra de unidad o un directorio de otro volumen.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Funciones de Volume-Scanning



| Función                                   | Descripción                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Devuelve el nombre de un volumen de un equipo. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) se usa para empezar a enumerar los volúmenes de un equipo. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continúa una búsqueda de volumen iniciada por una llamada a [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Cierra una búsqueda de volúmenes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funciones de examen de carpetas montadas



| Función                                                       | Descripción                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Recupera el nombre de una carpeta montada en el volumen especificado. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) se usa para empezar a examinar las carpetas montadas en un volumen. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Continúa una búsqueda de carpeta montada iniciada por una llamada a [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Cierra una búsqueda de carpetas montadas.                                                                                                                                                      |



 

 

 



