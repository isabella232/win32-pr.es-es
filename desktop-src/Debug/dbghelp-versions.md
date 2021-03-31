---
description: La biblioteca DbgHelp se implementa mediante DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versiones de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806956"
---
# <a name="dbghelp-versions"></a>Versiones de DbgHelp

La biblioteca DbgHelp se implementa mediante DbgHelp.dll. Aunque este archivo DLL se incluye en todas las versiones compatibles de Windows, rara vez está disponible la versión más reciente de DbgHelp. Además, la versión de DbgHelp que se incluye en Windows tiene una funcionalidad reducida de las otras versiones; en concreto, no se admite el servidor de símbolos y el servidor de origen.

Las versiones más recientes de DbgHelp.dll, SymSrv.dll y SrcSrv.dll están disponibles como parte del paquete de [herramientas de depuración para Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) . Las directivas de redistribución de estos archivos dll incluidos se diseñaron específicamente para que los usuarios lo puedan incluir en sus propios paquetes y versiones.

> [!Caution]  
> Los usuarios nunca deben intentar instalar las [herramientas de depuración para](https://developer.microsoft.com/windows/downloads/windows-10-sdk) las versiones de Windows de DbgHelp.dll en los directorios del sistema de Windows porque no se han probado en este escenario y es probable que desestabilicen el sistema. Hay versiones independientes de x64 y x86 del paquete de depuración, y las dos son necesarias para los usuarios interesados en admitir ambas plataformas.

Para obtener la versión más reciente de DbgHelp.dll, vaya a [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) y descargue herramientas de depuración para Windows. Consulte [llamada a la biblioteca DbgHelp](calling-the-dbghelp-library.md) para obtener información sobre la instalación correcta.

> [!Note]  
> El archivo DbgHelp.dll que se incluye en Windows no es redistribuible.

Muchas versiones de DbgHelp incluyen funcionalidad adicional. Para asegurarse de que la versión correcta de DbgHelp está disponible para su aplicación, revise la información de los requisitos en la documentación de referencia de la API específica.
