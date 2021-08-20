---
description: La función AreFileApisANSI determina si las funciones de E/S de archivo usan la página de códigos del juego de caracteres ANSI o OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinar la página de códigos del juego de caracteres actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150662"
---
# <a name="determining-the-current-character-set-code-page"></a>Determinar la página de códigos del juego de caracteres actual

La [**función AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina si las funciones de E/S de archivo usan la página de códigos del juego de caracteres ANSI o OEM. La [**función SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) hace que las funciones usen la página de códigos ANSI. La [**función SetFileApisToOEM hace**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) que las funciones usen la página de códigos de OEM.

De forma predeterminada, las funciones de E/S de archivo usan nombres de archivo ANSI. Las funciones exportadas por Kernel32.dll que aceptan o devuelven nombres de archivo se ven afectadas por la configuración de la página de códigos de archivo.

Tanto [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) como [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) establecen la página de códigos por proceso, en lugar de por subproceso o por equipo.

 

 



