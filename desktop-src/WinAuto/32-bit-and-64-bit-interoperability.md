---
title: interoperabilidad de 32 y 64 bits
description: Las aplicaciones de tecnología de asistencia necesitan comunicarse a través de los límites del proceso para obtener información de la interfaz de usuario de Microsoft Active Accessibility servidores y proveedores de automatización de la interfaz de usuario de Microsoft.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6897082db00e27d77d90e5fc72d5f229834ce760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792478"
---
# <a name="32-bit-and-64-bit-interoperability"></a>interoperabilidad de 32 y 64 bits

Las aplicaciones de tecnología de asistencia necesitan comunicarse a través de los límites del proceso para obtener información de la interfaz de usuario de Microsoft Active Accessibility servidores y proveedores de automatización de la interfaz de usuario de Microsoft. En este tema se describen los principales problemas de comunicación entre procesos que se deben tener en cuenta al desarrollar aplicaciones de accesibilidad de Windows.

Cuando las aplicaciones usan la API de automatización de Windows, los componentes de tiempo de ejecución de Microsoft Active Accessibility y de la automatización de la interfaz de usuario controlan automáticamente todos los problemas y las complejidades que conlleva la realización de comunicaciones entre procesos (IPC), incluidos los problemas de interoperabilidad implicados cuando un proceso es de 32 bits y el otro es de 64 bits. Microsoft reconoce que hay ocasiones en que una aplicación de tecnología de asistencia puede necesitar usar algún tipo de IPC en lugar de la API de automatización de Windows para comunicarse con un servidor de Microsoft Active Accessibility o un proveedor de automatización de la interfaz de usuario. En estas ocasiones, Microsoft recomienda que utilice mensajes DCOM o Windows (aquellos con valores menores que los de **\_ usuario de WM**) para comunicarse con otros procesos. Al igual que la API de automatización de Windows, los mensajes de Windows y DCOM controlan automáticamente todos los problemas de IPC, incluida la interoperabilidad de 32 bits a 64 bits.

Cuando la API de automatización de Windows, DCOM y los mensajes de Windows no son una opción, tenga en cuenta los siguientes problemas al implementar el método IPC elegido:

-   Memoria compartida: cuando se usa la memoria compartida, tenga en cuenta que una estructura en un proceso de 32 bits puede tener un diseño y un tamaño distintos que la misma estructura en un proceso de 64 bits. Esto es especialmente cierto en el caso de las estructuras que contienen punteros o identificadores.
-   Truncamiento de puntero: aunque una aplicación de 32 bits puede usar el tipo de datos **LONGLONG** para almacenar un valor de 64 bits, hay instancias en las que no existe ningún elemento de la API de Windows que permita a la aplicación de 32 bits recibir un valor de 64 bits de un proceso de 64 bits o enviar un valor de 64 bits a un proceso de 64 bits. Por ejemplo, las funciones [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) y [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) truncan todos los valores de puntero, lo que sale de la aplicación de 32 bits con un valor inútil.
-   Identificadores: dado que los identificadores Kernel32 y user32 32 solo son significativos en los procesos de 32 y 64 bits, se pueden transferir entre procesos sin problemas. Sin embargo, algunos elementos que Windows define como identificadores son simplemente punteros ajustados (por ejemplo, **HTREEITEM**). Estos "identificadores" se truncarán si se pasan de un proceso de 64 bits a un proceso de 32 bits.
-   [WinEvent](winevents-infrastructure.md) Funciones de enlace: para registrar una función de enlace en contexto con un proceso de servidor de 32 bits, la función de enlace debe residir en un archivo DLL de 32 bits. Del mismo modo, para registrar una función de enlace en contexto con un proceso de servidor de 64 bits, la función de enlace debe residir en un archivo DLL de 64 bits. Si una aplicación de tecnología de asistencia intenta registrar una función de enlace en contexto con un servidor que tiene una profundidad de bits diferente, los eventos se seguirán entregando a la función de enlace, pero se entregarán fuera de contexto. Para obtener más información, consulte WinEvents y [funciones de enlace en contexto y fuera de contexto](in-context-and-out-of-context-hook-functions.md).

Para obtener más información sobre la interoperabilidad de 32 y 64 bits, consulte [interoperabilidad de procesos](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la API de automatización de Windows](windows-automation-api-overview.md)
</dt> </dl>

 

 