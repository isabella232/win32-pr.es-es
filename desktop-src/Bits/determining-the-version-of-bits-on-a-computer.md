---
title: Determinar la versión de BITS en un equipo
description: Para determinar la versión de BITS en el equipo cliente, compruebe la versión de QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caa2c501fd5f37d44becf11679debb1390aeeb9ee47bee02b43a97788493cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005315"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Determinar la versión de BITS en un equipo

Para determinar la versión de BITS en el equipo cliente, compruebe la versión de QMgr.dll. Para buscar el número de versión del archivo DLL:

-   Busque QMgr.dll %windir% \\ System32.
-   Haga clic con el botón QMgr.dll haga clic en **Propiedades.**
-   Haga clic en **la pestaña** Versión.
-   Anote el número de versión.

También puede usar el siguiente código de PowerShell para determinar la versión del .dll en el sistema:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Si el archivo DLL también existe en %windir% \\ System32 \\ Bits, repita los pasos anteriores. BITS usa el archivo DLL con el número de versión superior.

En la tabla siguiente se enumeran las versiones de BITS y sus correspondientes QMgr.dll de versión del archivo.



| Versión de BITS | QMgr.dll de versión del archivo |
|--------------|------------------------------|
| BITS 10.1    | 7.8.xxxx.xxxx                |
| BITS 5.0     | 7.7.xxxx.xxxx                |
| BITS 4.0     | 7.5.xxxx.xxxx                |
| BITS 3.0     | 7.0.xxxx.xxxx                |
| BITS 2.5     | 6.7.xxxx.xxxx                |
| BITS 2.0     | 6.6.xxxx.xxxx                |
| BITS 1.5     | 6.5.xxxx.xxxx                |
| BITS 1.2     | 6.2.xxxx.xxxx                |
| BITS 1.0     | 6.0.xxxx.xxxx                |



 

También puede usar los identificadores de clase simbólicos para determinar la versión de BITS registrada en el equipo. En la tabla siguiente se enumeran las versiones de BITS y sus identificadores de clase simbólica correspondientes. La **función CoCreateInstance** devuelve **REGDB E \_ \_ CLASSNOTREG** si la clase no está registrada.



| Versión de BITS  | Identificador de clase simbólico         |
|---------------|-----------------------------------|
| BITS 10.1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5.0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4.0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3.0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2.0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1.5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1.2, 1.0 | CLSID \_ BackgroundCopyManager      |



 

 

 




