---
description: La biblioteca DbgHelp se implementa mediante DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versiones de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343865"
---
# <a name="dbghelp-versions"></a>Versiones de DbgHelp

La biblioteca DbgHelp se implementa mediante DbgHelp.dll. Aunque este archivo DLL se incluye en todas las versiones admitidas de Windows, rara vez es la versión más reciente de DbgHelp disponible. Además, la versión de DbgHelp que se incluye en Windows ha reducido la funcionalidad de las otras versiones; en concreto, carece de compatibilidad con el servidor de símbolos y el servidor de origen.

Las versiones más recientes de DbgHelp.dll, SymSrv.dll y SrcSrv.dll están disponibles como parte de las herramientas de depuración [para Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) paquete. Las directivas de redistribución para estos archivos DLL incluidos se diseñaron específicamente para que los usuarios puedan incluir estos archivos lo más fácilmente posible en sus propios paquetes y versiones.

> [!Caution]  
> Los usuarios nunca deben intentar instalar las herramientas de depuración para las versiones de [Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) de DbgHelp.dll en los directorios del sistema de Windows porque no se han probado en este escenario y es probable que desestabilicen el sistema. Hay versiones X64 y X86 independientes del paquete de depuración y ambas son necesarias para las personas interesadas en admitir ambas plataformas.

Para obtener la versión más reciente de DbgHelp.dll, vaya a [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) y descargue Herramientas de depuración para Windows. Consulte Llamada [a la biblioteca DbgHelp para](calling-the-dbghelp-library.md) obtener información sobre la instalación correcta.

> [!Note]  
> El DbgHelp.dll que se incluye en Windows no es redistribuible.

Muchas versiones de DbgHelp incluyen funcionalidad adicional. Para asegurarse de que la versión correcta de DbgHelp está disponible para la aplicación, revise la información de requisitos en la documentación de referencia de API específica.
