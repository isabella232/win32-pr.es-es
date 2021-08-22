---
description: IMM incluye la comprobación de identificación de subprocesos que determina si un subproceso que realiza la llamada es el creador de un identificador de contexto de método de entrada especificado (tipo HIMC) o un identificador de ventana (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Desarrollo de IME-Aware aplicaciones de varios subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf495922d347119db3b8b517af13c850f2f19dfc558609f93f24953f0a3386a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949600"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Desarrollo de IME-Aware aplicaciones de varios subprocesos

IMM incluye la comprobación de identificación de subprocesos que determina si un subproceso que realiza la llamada es el creador de un identificador de contexto de método de entrada especificado (tipo HIMC) o un identificador de ventana (tipo HWND). Si el subproceso no es el creador del identificador, se produce un error en la función IMM llamada y una llamada posterior a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ INVALID \_ ACCESS.

> [!Note]  
> La arquitectura IMM actual no proporciona una instalación de sincronización para el acceso a los identificadores de IMM.

 

Para usar la comprobación de identificación de subprocesos, las aplicaciones deben cumplir las siguientes directrices:

-   Un subproceso no debe tener acceso al contexto de entrada creado por otro subproceso.
-   Un subproceso no debe asociar un contexto de entrada a una ventana creada por otro subproceso, y viceversa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
