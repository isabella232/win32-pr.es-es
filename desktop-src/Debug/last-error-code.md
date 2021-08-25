---
description: Cuando se produce un error, la mayoría de las funciones del sistema devuelven un código de error, normalmente 0, NULL o \# &8211;1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Last-Error code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd3f7a202f4ed67105620a7d2688cfa278fbdc127ed942861de0d69517e96620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912555"
---
# <a name="last-error-code"></a>Last-Error code

Cuando se produce un error, la mayoría de las funciones del sistema devuelven un código de error, normalmente 0, **NULL** o –1. Muchas funciones del sistema también establecen un código de error adicional denominado *código de último error.* Este código de error se mantiene por separado para cada subproceso en ejecución; Un error en un subproceso no sobrescribe el código del último error en otro subproceso. Cualquier función puede llamar a [**las funciones SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) o [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) para establecer el código de último error para el subproceso actual. Estas funciones están diseñadas principalmente para bibliotecas de vínculos dinámicos (DLL), por lo que pueden proporcionar información a la aplicación que realiza la llamada. Tenga en cuenta que algunas funciones llaman a **SetLastError** o **SetLastErrorEx** con 0 cuando se realiza correctamente, lo que borrará el código de error establecido por la función con error más reciente, mientras que otras no.

Una aplicación puede recuperar el código del último error mediante la [**función GetLastError;**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) el código de error puede decir más sobre lo que realmente se produjo para que se produjese un error en la función. La documentación de las funciones del sistema indicará las condiciones en las que la función establece el código del último error.

El sistema define un conjunto de códigos de error que se pueden establecer como códigos de último error o ser devueltos por estas funciones. Los códigos de error son valores de 32 bits (el bit 31 es el bit más significativo). El bit 29 está reservado para los códigos de error definidos por la aplicación; ningún código de error del sistema tiene este conjunto de bits. Si define códigos de error para la aplicación, establezca este bit para indicar que una aplicación ha definido el código de error y para asegurarse de que los códigos de error no entren en conflicto con ningún código de error definido por el sistema. Para obtener más información, vea WinError.h y [Códigos de error del sistema](system-error-codes.md).

 

 
