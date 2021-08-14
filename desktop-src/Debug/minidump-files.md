---
description: Las aplicaciones pueden generar archivos de minivolca en modo de usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado de memoria.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Archivos de minivolfón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412e719d54f34c9766981667be35990c37ae3511eaecc8836ceac0311a5105e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406095"
---
# <a name="minidump-files"></a>Archivos de minivolfón

Las aplicaciones pueden generar archivos de minivolca en modo de usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado de memoria. Las aplicaciones pueden crear archivos de minivolfón de forma muy rápida y eficaz. Dado que los archivos de minivolquete son pequeños, se pueden enviar fácilmente a través de Internet al soporte técnico de la aplicación.

Un archivo de minivolca no contiene tanta información como un archivo de volcado de memoria completo, pero contiene suficiente información para realizar operaciones de depuración básicas. Para leer un archivo de minivolumen, debe tener los archivos binarios y los archivos de símbolos disponibles para el depurador.

Las versiones actuales de Microsoft Office y Microsoft Windows crear archivos de minivolumen con el fin de analizar los errores en los equipos de los clientes.

Las siguientes funciones dbgHelp se usan con archivos de minivolfón.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



