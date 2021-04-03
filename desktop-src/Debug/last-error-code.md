---
description: Cuando se produce un error, la mayoría de las funciones del sistema devuelven un código de error, normalmente 0, NULL o &\# 8211; 1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Código de Last-Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bf0fe2f544fc3d87690be81b0d09767745ef95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998145"
---
# <a name="last-error-code"></a>Código de Last-Error

Cuando se produce un error, la mayoría de las funciones del sistema devuelven un código de error, normalmente 0, **null** o – 1. Muchas funciones del sistema también establecen un código de error adicional denominado *código de último error*. Este código de error se mantiene por separado para cada subproceso en ejecución; un error en un subproceso no sobrescribe el código de último error en otro subproceso. Cualquier función puede llamar a la función [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) o [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) para establecer el último código de error del subproceso actual. Estas funciones están pensadas principalmente para las bibliotecas de vínculos dinámicos (DLL), por lo que pueden proporcionar información a la aplicación que realiza la llamada. Tenga en cuenta que algunas funciones llaman a **SetLastError** o **SetLastErrorEx** con 0 cuando se ejecutan correctamente, borrando el código de error establecido por la función con error más reciente, mientras que otros no.

Una aplicación puede recuperar el código de último error mediante la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . el código de error puede indicar más información sobre lo que se produjo realmente para que se produzca un error en la función. La documentación de las funciones del sistema indicará las condiciones en las que la función establece el código de último error.

El sistema define un conjunto de códigos de error que se pueden establecer como códigos de último error o que pueden ser devueltos por estas funciones. Los códigos de error son valores de 32 bits (el bit 31 es el bit más significativo). El bit 29 está reservado para los códigos de error definidos por la aplicación; ningún código de error del sistema tiene este bit establecido. Si define los códigos de error de la aplicación, establezca este bit para indicar que una aplicación ha definido el código de error y para asegurarse de que los códigos de error no entran en conflicto con los códigos de error definidos por el sistema. Para obtener más información, consulte WinError. h y [códigos de error del sistema](system-error-codes.md).

 

 
