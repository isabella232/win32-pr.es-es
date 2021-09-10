---
title: Uso compartido de un procedimiento de E/S con otras aplicaciones
description: Uso compartido de un procedimiento de E/S con otras aplicaciones
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- E/S de archivos multimedia, procedimientos compartidos
- E/S de archivo, procedimientos compartidos
- entrada y salida (E/S), procedimientos compartidos
- E/S (entrada y salida), procedimientos compartidos
- uso compartido de procedimientos de E/S con otras aplicaciones
- Función mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371834"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>Uso compartido de un procedimiento de E/S con otras aplicaciones

Si desea compartir un procedimiento de E/S con otras aplicaciones, debe escribir una biblioteca de vínculos dinámicos (DLL) para la aplicación. Puede compartir el procedimiento de E/S realizando una de las siguientes acciones:

-   Incluya el código para el procedimiento de E/S en el archivo DLL.
-   Cree una función en el archivo DLL que llame a la [**función mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) para instalar el procedimiento de E/S.
-   Exporte esta función en el archivo module-definitions del archivo DLL.

Para usar el procedimiento de E/S compartido, una aplicación debe llamar primero a la función en el archivo DLL para instalar el procedimiento de E/S.

 

 