---
description: Las aplicaciones pueden generar archivos de minivolcado en modo usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Archivos de minivolcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152849"
---
# <a name="minidump-files"></a>Archivos de minivolcado

Las aplicaciones pueden generar archivos de minivolcado en modo usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado. Las aplicaciones pueden crear archivos de minivolcado de manera muy rápida y eficaz. Dado que los archivos de minivolcado son pequeños, se pueden enviar fácilmente a través de Internet a soporte técnico para la aplicación.

Un archivo de minivolcado no contiene tanta información como un archivo de volcado de memoria completo, pero contiene suficiente información para realizar operaciones de depuración básicas. Para leer un archivo de minivolcado, debe tener los archivos binarios y de símbolos disponibles para el depurador.

Las versiones actuales de Microsoft Office y Microsoft Windows crean archivos de minivolcado con el fin de analizar los errores en los equipos de los clientes.

Las siguientes funciones DbgHelp se utilizan con archivos de minivolcado.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



