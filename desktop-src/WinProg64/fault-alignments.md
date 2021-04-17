---
title: Errores de alineación
description: Errores de alineación
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- errores de alineación 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714429"
---
# <a name="alignment-faults"></a>Errores de alineación

El controlador de errores de alineación del sistema está desactivado de forma predeterminada en los sistemas basados en Itanium. Por lo tanto, cualquier acceso a datos no alineado genera una excepción que el sistema no solucionará automáticamente a menos que la aplicación detecte la excepción en un [controlador de excepciones basado en marcos](/windows/desktop/Debug/frame-based-exception-handling). Para habilitar el controlador de errores de alineación del sistema, llame a la función [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) con **SEM \_ NOALIGNMENTFAULTEXCEPT**. Sin embargo, tenga en cuenta que los procesos pueden experimentar una degradación grave del rendimiento si está habilitado el controlador de errores de alineación del sistema y el proceso genera errores de alineación.

Si el depurador WinDbg se ha instalado como el depurador del sistema, WinDbg se iniciará automáticamente si algún proceso del sistema genera una excepción no controlada. Si no tiene un depurador instalado como depurador del sistema, el sistema muestra un cuadro de diálogo que indica que la aplicación ha encontrado un error y proporciona la oportunidad de notificar el problema a Microsoft.

En los sistemas x64 y ARM64, cualquier error de alineación se controla mediante una combinación de hardware y software. Para obtener el mejor rendimiento, todo el acceso a la memoria debe estar correctamente alineado. Además, el [acceso a la variable entrelazada](/windows/desktop/Sync/interlocked-variable-access) no alineada debe evitarse en ARM64, ya que estas operaciones no son seguras para atomicidad.

 

 