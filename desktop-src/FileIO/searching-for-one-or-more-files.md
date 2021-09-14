---
description: Una aplicación puede buscar en el directorio actual todos los nombres de archivo que coincidan con un patrón determinado mediante las funciones FindFirstFile, FindFirstFileEx, FindNextFile y FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Buscar uno o varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069848"
---
# <a name="searching-for-one-or-more-files"></a>Buscar uno o varios archivos

Una aplicación puede buscar en el directorio actual todos los nombres de archivo que coincidan con un patrón determinado mediante las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx,**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)y [**FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) El patrón debe ser un nombre de archivo válido y puede incluir caracteres comodín.

Las [**funciones FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) crean identificadores que **FindFirstFileEx** usa para buscar otros archivos con el mismo patrón. Todas las funciones devuelven información sobre el archivo que se encontró. Esta información incluye el nombre de archivo, el tamaño, los atributos y la hora.

La [**función FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) también permite que una aplicación busque archivos en función de criterios de búsqueda adicionales. La función puede limitar las búsquedas a nombres de dispositivo o nombres de directorio.

La [**función FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) destruye los identificadores creados [**por FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindFirstFileEx.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)

Una aplicación puede buscar un solo archivo en una ruta de acceso específica mediante la [**función SearchPath.**](/windows/win32/api/processenv/nf-processenv-searchpatha)

 

 
