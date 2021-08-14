---
title: Errores de alineación
description: Errores de alineación
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- errores de alineación de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d813a47cb3428c57ee6235442491f26f8d126a997dd7fcfa6844d551e7958b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412915"
---
# <a name="alignment-faults"></a>Errores de alineación

El controlador de errores de alineación del sistema está desactivado de forma predeterminada en los sistemas basados en Itanium. Por lo tanto, cualquier acceso a datos no alineado genera una excepción que el sistema no solucionará automáticamente a menos que la aplicación detecta la excepción en un controlador de excepciones basado [en marco.](/windows/desktop/Debug/frame-based-exception-handling) Para habilitar el hander de error de alineación del sistema, llame a la [**función SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) **con SEM \_ NOALIGNMENTFAULTEXCEPT**. Sin embargo, tenga en cuenta que los procesos pueden experimentar una degradación grave del rendimiento si el controlador de errores de alineación del sistema está habilitado y el proceso genera errores de alineación.

Si el depurador de WinDbg se ha instalado como depurador del sistema, WinDbg se iniciará automáticamente si algún proceso del sistema genera una excepción no controlada. Si no tiene un depurador instalado como depurador del sistema, el sistema muestra un cuadro de diálogo que indica que la aplicación ha encontrado un error y proporciona la oportunidad de notificar el problema a Microsoft.

En los sistemas x64 y ARM64, los errores de alineación se controlan mediante una combinación de hardware y software. Para obtener el mejor rendimiento, todo el acceso a la memoria debe estar alineado correctamente. Además, se debe evitar el acceso a [variables](/windows/desktop/Sync/interlocked-variable-access) no alineadas entrelazados en ARM64, ya que estas operaciones no son seguras atómicamente.

 

 