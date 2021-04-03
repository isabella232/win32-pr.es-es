---
description: Bloque de entorno de subprocesos (notas de depuración)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloque de entorno de subprocesos (notas de depuración)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907237"
---
# <a name="thread-environment-block-debugging-notes"></a>Bloque de entorno de subprocesos (notas de depuración)

El bloque de entorno de subprocesos ([**estructura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contiene información de contexto para un subproceso.

En las siguientes versiones de Windows, el desplazamiento de la dirección TEB de 32 bits en el TEB de 64 bits es 0. Se puede usar para tener acceso directamente al TEB de 32 bits de un subproceso de WOW64. Esto podría cambiar en versiones posteriores de Windows



|               |                        |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras de depuración](debugging-structures.md)
</dt> <dt>

[**Contexto de WOW64 \_**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
