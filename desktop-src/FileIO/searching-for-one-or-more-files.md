---
description: Una aplicación puede buscar en el directorio actual todos los nombres de archivo que coinciden con un patrón determinado mediante las funciones FindFirstFile, FindFirstFileEx, FindNextFile y FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Buscar uno o varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687010"
---
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="2de5d-103">Buscar uno o varios archivos</span><span class="sxs-lookup"><span data-stu-id="2de5d-103">Searching for One or More Files</span></span>

<span data-ttu-id="2de5d-104">Una aplicación puede buscar en el directorio actual todos los nombres de archivo que coinciden con un patrón determinado mediante las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)y [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="2de5d-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="2de5d-105">El patrón debe ser un nombre de archivo válido y puede incluir caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="2de5d-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="2de5d-106">Las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) crean identificadores que usa **FindFirstFileEx** para buscar otros archivos con el mismo patrón.</span><span class="sxs-lookup"><span data-stu-id="2de5d-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="2de5d-107">Todas las funciones devuelven información sobre el archivo que se encontró.</span><span class="sxs-lookup"><span data-stu-id="2de5d-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="2de5d-108">Esta información incluye el nombre de archivo, el tamaño, los atributos y la hora.</span><span class="sxs-lookup"><span data-stu-id="2de5d-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="2de5d-109">La función [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) también permite que una aplicación busque archivos en función de criterios de búsqueda adicionales.</span><span class="sxs-lookup"><span data-stu-id="2de5d-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="2de5d-110">La función puede limitar las búsquedas a nombres de dispositivo o de directorio.</span><span class="sxs-lookup"><span data-stu-id="2de5d-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="2de5d-111">La función [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) destruye los identificadores creados por [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span><span class="sxs-lookup"><span data-stu-id="2de5d-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="2de5d-112">Una aplicación puede buscar un único archivo en una ruta de acceso específica mediante la función [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .</span><span class="sxs-lookup"><span data-stu-id="2de5d-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
