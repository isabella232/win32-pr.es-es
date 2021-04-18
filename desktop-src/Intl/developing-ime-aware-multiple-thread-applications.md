---
description: El IMM incluye la comprobación de identificación de subprocesos que determina si un subproceso que realiza la llamada es el creador de un identificador de contexto de método de entrada especificado (tipo HIMC) o un identificador de ventana (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Desarrollar IME-Aware aplicaciones de varios subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688350"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Desarrollar IME-Aware aplicaciones de varios subprocesos

El IMM incluye la comprobación de identificación de subprocesos que determina si un subproceso que realiza la llamada es el creador de un identificador de contexto de método de entrada especificado (tipo HIMC) o un identificador de ventana (tipo HWND). Si el subproceso no es el creador del identificador, se produce un error en la función denominada IMM y una llamada subsiguiente a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ acceso no válido \_ .

> [!Note]  
> La arquitectura de IMM actual no proporciona una utilidad de sincronización para el acceso a los identificadores de IMM.

 

Para usar la comprobación de identificación de subprocesos, las aplicaciones deben cumplir las siguientes directrices:

-   Un subproceso no debe tener acceso al contexto de entrada creado por otro subproceso.
-   Un subproceso no debe asociar un contexto de entrada a una ventana creada por otro subproceso, y viceversa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
