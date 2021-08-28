---
description: Bloque de entorno de subprocesos (notas de depuración)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloque de entorno de subprocesos (notas de depuración)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f5c40b2a64eb868a7fd3ffb2052a3692db90f19d33357d4ef4f3113803bf52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655275"
---
# <a name="thread-environment-block-debugging-notes"></a>Bloque de entorno de subprocesos (notas de depuración)

El bloque de entorno de subproceso [**(estructura TEB)**](/windows/win32/api/winternl/ns-winternl-teb)contiene información de contexto para un subproceso.

En las siguientes versiones de Windows, el desplazamiento de la dirección TEB de 32 bits dentro del TEB de 64 bits es 0. Se puede usar para acceder directamente al TEB de 32 bits de un subproceso WOW64. Esto puede cambiar en versiones posteriores de Windows



|  Plataforma     | Versión                |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras de depuración](debugging-structures.md)
</dt> <dt>

[**CONTEXTO \_ WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
