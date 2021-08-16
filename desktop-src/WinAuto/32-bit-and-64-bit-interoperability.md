---
title: Interoperabilidad de 32 y 64 bits
description: Las aplicaciones de tecnología de asistencia necesitan comunicarse a través de los límites del proceso para obtener información de la interfaz de usuario de Microsoft Active Accessibility servidores y proveedores de Automatización de la interfaz de usuario Microsoft.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c056c9fe2792734e9369fa311e69528ce226f7edf15b82440b63c12c52de66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327994"
---
# <a name="32-bit-and-64-bit-interoperability"></a>Interoperabilidad de 32 y 64 bits

Las aplicaciones de tecnología de asistencia necesitan comunicarse a través de los límites del proceso para obtener información de la interfaz de usuario de Microsoft Active Accessibility servidores y proveedores de Automatización de la interfaz de usuario Microsoft. En este tema se describen los principales problemas de comunicación entre procesos que debe tener en cuenta al desarrollar Windows de accesibilidad.

Cuando las aplicaciones usan la API de automatización de Windows, los componentes en tiempo de ejecución de Microsoft Active Accessibility y Automatización de la interfaz de usuario controlan automáticamente todos los problemas y complejidades implicados en la realización de comunicaciones entre procesos (IPC), incluidos los problemas de interoperabilidad implicados cuando un proceso tiene 32 bits y el otro es de 64 bits. Microsoft reconoce que hay ocasiones en las que una aplicación de tecnología de asistencia puede necesitar usar algún tipo de IPC en lugar de la API de automatización de Windows para comunicarse con un servidor Microsoft Active Accessibility o un proveedor Automatización de la interfaz de usuario. En estas ocasiones, Microsoft recomienda usar mensajes DCOM o Windows (aquellos con valores menores que los de **WM \_ USER)** para comunicarse con otros procesos. Al igual que Windows Automation API, los mensajes DCOM y Windows controlan automáticamente todos los problemas de IPC, incluida la interoperabilidad de 32 bits a 64 bits.

Cuando los Windows Automation API, DCOM y Windows no son una opción, tenga en cuenta los siguientes problemas al implementar el método IPC elegido:

-   Memoria compartida: al usar memoria compartida, tenga en cuenta que una estructura en un proceso de 32 bits puede tener un tamaño y un diseño diferentes a los de la misma estructura en un proceso de 64 bits. Esto es especialmente cierto para las estructuras que contienen punteros o identificadores.
-   Truncamiento de puntero: aunque una aplicación de 32 bits puede usar el tipo de datos **LONGLONG** para almacenar un valor de 64 bits, hay instancias en las que no existe ningún elemento de API de Windows que permita que la aplicación de 32 bits reciba un valor de 64 bits de un proceso de 64 bits o envíe un valor de 64 bits a un proceso de 64 bits. Por ejemplo, las [**funciones GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) y [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) truncan todos los valores de puntero, dejando a la aplicación de 32 bits con un valor inservible.
-   Identificadores: dado que los identificadores kernel32 y user32 solo son significativos de 32 bits en procesos de 32 y 64 bits, se pueden transferir entre procesos sin problemas. Sin embargo, algunos elementos que Windows definen como identificadores son simplemente punteros encapsulados (por ejemplo, **HTREEITEM**). Estos "identificadores" se truncarán si se pasan de un proceso de 64 bits a un proceso de 32 bits.
-   [WinEvent](winevents-infrastructure.md) Funciones de enlace: para registrar una función de enlace en contexto con un proceso de servidor de 32 bits, la función de enlace debe residir en un archivo DLL de 32 bits. De forma similar, para registrar una función de enlace en contexto con un proceso de servidor de 64 bits, la función de enlace debe residir en un archivo DLL de 64 bits. Si una aplicación de tecnología de asistencia intenta registrar una función de enlace en contexto con un servidor con una profundidad de bits diferente, los eventos se seguirán entregando a la función de enlace, pero se entregarán fuera de contexto. Para obtener más información, vea WinEvents and [In-Context and Out-of-Context Hook Functions](in-context-and-out-of-context-hook-functions.md).

Para obtener más información sobre la interoperabilidad de 32 y 64 bits, vea [Interoperabilidad de procesos.](/windows/desktop/WinProg64/process-interoperability)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Introducción a la API de Automation](windows-automation-api-overview.md)
</dt> </dl>

 

 