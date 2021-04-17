---
title: Interoperabilidad del proceso
description: Puede ejecutar aplicaciones basadas en Win32 en Windows de 64 bits con una capa de emulación. Windows 10 en ARM incluye una capa de emulación x86-on-ARM64. Para obtener más información, vea ejecutar aplicaciones de 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- Programación de la interoperabilidad de Windows de 64 bits
- interoperabilidad de la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704683"
---
# <a name="process-interoperability"></a>Interoperabilidad del proceso

Puede ejecutar aplicaciones basadas en Win32 en Windows de 64 bits con una capa de emulación. Windows 10 en ARM incluye una capa de emulación x86-on-ARM64. Para obtener más información, vea [ejecutar aplicaciones de 32 bits](running-32-bit-applications.md).

En Windows de 64 bits, un proceso de 64 bits no puede cargar una biblioteca de vínculos dinámicos (DLL) de 32 bits. Además, un proceso de 32 bits no puede cargar un archivo DLL de 64 bits. Sin embargo, Windows de 64 bits admite llamadas a procedimiento remoto (RPC) entre procesos de 64 bits y de 32 bits (tanto en el mismo equipo como en varios equipos). En Windows de 64 bits, un servidor COM fuera de proceso de 32 bits puede comunicarse con un cliente de 64 bits y un servidor COM de 64 bits fuera de proceso puede comunicarse con un cliente de 32 bits. Por lo tanto, si tiene una DLL de 32 bits que no es compatible con COM, puede encapsularla en un servidor COM fuera de proceso y utilizar COM para serializar las llamadas a y desde un proceso de 64 bits.

Los servidores en proceso están registrados actualmente mediante la entrada del registro **InprocServer** . En Windows de 64 bits, los servidores en proceso de 64 y 32 deben usar la entrada **InProcServer32** .

Para los identificadores de puerto, que por su naturaleza son locales para el equipo y que nunca se utilizarán en el límite de 32 bits a 64 bits, utilice el tipo **\_ ptr de identificador** en lugar del tipo de PTR **int \_** o **DWORD \_** . Esto incluye la migración de interfaces RPC que pasan tales identificadores como valores **DWORD** . El **identificador \_ PTR** de 64 bits es de 64 bits en la conexión (no truncado) y, por tanto, no necesita asignación. (El **\_ puntero de identificador** de 32 bits es de 32 bits en la conexión).

Para obtener más información, vea [diseñar interfaces compatibles con 64 bits](designing-64-bit-compatible-interfaces.md).

 

 




