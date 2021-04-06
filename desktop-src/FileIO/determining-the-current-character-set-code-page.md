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
# <a name="determining-the-current-character-set-code-page"></a>Determinar la página de códigos del juego de caracteres actual

La función [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina si las funciones de e/s de archivo usan la página de códigos del juego de caracteres ANSI o OEM. La función [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) hace que las funciones usen la página de códigos ANSI. La función [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) hace que las funciones usen la página de códigos OEM.

De forma predeterminada, las funciones de e/s de archivo utilizan nombres de archivo ANSI. La configuración de la página de códigos del archivo afecta a las funciones exportadas por Kernel32.dll que aceptan o devuelven nombres de archivo.

Tanto [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) como [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) establecen la página de códigos por proceso, en lugar de por subproceso o por equipo.

 

 



