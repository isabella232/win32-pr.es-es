---
description: Funciones que se usan para administrar carpetas montadas.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funciones de carpeta montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13175dc4846d8f8438a3f1b94b3e407aaf347e2b6d10ad5c3761899882ecdfaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870785"
---
# <a name="mounted-folder-functions"></a>Funciones de carpeta montadas

Las funciones de carpeta montadas se pueden dividir en tres grupos: funciones de uso general, funciones que se usan para buscar volúmenes y funciones que se usan para examinar un volumen en busca de carpetas montadas.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose de carpeta montada



| Función                                                                     | Descripción                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Elimina una letra de unidad o una carpeta montada.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Recupera la ruta de acceso guid del volumen para el volumen asociado al punto de montaje de volumen especificado (letra de unidad, ruta de acceso GUID del volumen o carpeta montada). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Recupera la carpeta montada asociada al volumen especificado.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Asocia un volumen con una letra de unidad o un directorio en otro volumen.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Volume-Scanning Functions



| Función                                   | Descripción                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Devuelve el nombre de un volumen en un equipo. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) se usa para empezar a enumerar los volúmenes de un equipo. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continúa una búsqueda de volúmenes iniciada por una llamada a [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Cierra una búsqueda de volúmenes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funciones de examen de carpetas montadas



| Función                                                       | Descripción                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Recupera el nombre de una carpeta montada en el volumen especificado. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) se usa para empezar a examinar las carpetas montadas en un volumen. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Continúa una búsqueda de carpetas montada iniciada por una llamada a [**FindFirstVolumeMountPoint.**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Cierra una búsqueda de carpetas montadas.                                                                                                                                                      |



 

 

 



