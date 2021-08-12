---
title: Interoperabilidad de procesos
description: Puede ejecutar aplicaciones basadas en Win32 en aplicaciones de 64 Windows mediante una capa de emulación. Windows 10 en ARM incluye una capa de emulación x86 en ARM64. Para obtener más información, vea Ejecutar aplicaciones de 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- interoperabilidad de procesos de 64 bits Windows programación
- interoperabilidad de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74e75af4299e9c249ea46b8eac2cdd47de10eb3f832aa88d6b313d20304afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561521"
---
# <a name="process-interoperability"></a>Interoperabilidad de procesos

Puede ejecutar aplicaciones basadas en Win32 en aplicaciones de 64 Windows mediante una capa de emulación. Windows 10 en ARM incluye una capa de emulación x86 en ARM64. Para obtener más información, vea [Ejecutar aplicaciones de 32 bits.](running-32-bit-applications.md)

En un proceso de 64 Windows, un proceso de 64 bits no puede cargar una biblioteca de vínculos dinámicos (DLL) de 32 bits. Además, un proceso de 32 bits no puede cargar un archivo DLL de 64 bits. Sin embargo, el Windows de 64 bits admite llamadas a procedimiento remoto (RPC) entre procesos de 64 y 32 bits (tanto en el mismo equipo como entre equipos). En Windows de 64 bits, un servidor COM de 32 bits fuera de proceso puede comunicarse con un cliente de 64 bits y un servidor COM de 64 bits fuera de proceso puede comunicarse con un cliente de 32 bits. Por lo tanto, si tiene un archivo DLL de 32 bits que no es consciente de COM, puede encapsularlo en un servidor COM fuera de proceso y usar COM para serializar las llamadas a y desde un proceso de 64 bits.

Los servidores en proceso se registran actualmente mediante la entrada del Registro **InprocServer.** En servidores en proceso de 64 Windows, los servidores en proceso de 64 y 32 bits deben usar la **entrada InprocServer32.**

Para los identificadores de puerto, que por su naturaleza son locales en el equipo y nunca se usarían a través del límite de 32 bits a 64 bits, use el tipo **\_ HANDLE PTR** en lugar del tipo **INT \_ PTR** o **DWORD \_ PTR.** Esto incluye el porte de interfaces RPC que pasan estos identificadores como **valores DWORD.** Handle **\_ PTR** de 64 bits es de 64 bits en la conexión (no truncado) y, por tanto, no necesita asignación. (El HANDLE **\_ PTR** de 32 bits es de 32 bits en la conexión).

Para obtener más información, vea Diseño de interfaces compatibles con [64 bits.](designing-64-bit-compatible-interfaces.md)

 

 




