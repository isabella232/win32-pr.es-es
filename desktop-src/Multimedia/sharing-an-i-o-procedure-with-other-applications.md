---
title: Compartir un procedimiento de e/s con otras aplicaciones
description: Compartir un procedimiento de e/s con otras aplicaciones
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- e/s de archivos multimedia, procedimientos compartidos
- e/s de archivos, procedimientos compartidos
- entrada y salida (e/s), procedimientos compartidos
- E/s (entrada y salida), procedimientos compartidos
- compartir procedimientos de e/s con otras aplicaciones
- mmioInstallIOProc función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420594"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>Compartir un procedimiento de e/s con otras aplicaciones

Si desea compartir un procedimiento de e/s con otras aplicaciones, debe escribir una biblioteca de vínculos dinámicos (DLL) para la aplicación. Puede compartir el procedimiento de e/s mediante una de las siguientes acciones:

-   Incluya el código para el procedimiento de e/s en el archivo DLL.
-   Cree una función en el archivo DLL que llame a la función [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) para instalar el procedimiento de e/s.
-   Exporte esta función en el archivo de definiciones de módulo de la DLL.

Para usar el procedimiento de e/s compartido, una aplicación debe llamar primero a la función en el archivo DLL para instalar el procedimiento de e/s.

 

 