---
description: La función AreFileApisANSI determina si las funciones de e/s de archivo usan la página de códigos del juego de caracteres ANSI o OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinar la página de códigos del juego de caracteres actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910162"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="60e44-103">Determinar la página de códigos del juego de caracteres actual</span><span class="sxs-lookup"><span data-stu-id="60e44-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="60e44-104">La función [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina si las funciones de e/s de archivo usan la página de códigos del juego de caracteres ANSI o OEM.</span><span class="sxs-lookup"><span data-stu-id="60e44-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="60e44-105">La función [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) hace que las funciones usen la página de códigos ANSI.</span><span class="sxs-lookup"><span data-stu-id="60e44-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="60e44-106">La función [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) hace que las funciones usen la página de códigos OEM.</span><span class="sxs-lookup"><span data-stu-id="60e44-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="60e44-107">De forma predeterminada, las funciones de e/s de archivo utilizan nombres de archivo ANSI.</span><span class="sxs-lookup"><span data-stu-id="60e44-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="60e44-108">La configuración de la página de códigos del archivo afecta a las funciones exportadas por Kernel32.dll que aceptan o devuelven nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="60e44-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="60e44-109">Tanto [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) como [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) establecen la página de códigos por proceso, en lugar de por subproceso o por equipo.</span><span class="sxs-lookup"><span data-stu-id="60e44-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



