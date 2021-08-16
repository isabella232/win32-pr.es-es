---
description: Funciones de depuración de espera
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funciones de depuración de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049205"
---
# <a name="wait-debugging-functions"></a>Funciones de depuración de espera

Microsoft DirectShow proporciona varias funciones para depurar esperas infinitas.

En las compilaciones comerciales, las funciones [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) y [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionan como sus homólogos de API de Windows, **WaitForMultipleObjects** y **WaitForSingleObject,** con intervalos de tiempo de espera infinitos.

En las compilaciones de depuración, estas funciones usan un valor de tiempo de espera global. Si expira el tiempo de espera, la función desencadena una aserción. La siguiente clave del Registro especifica el valor de tiempo de espera, en milisegundos:

**HKEY \_ LOCAL \_ MACHINE \\ <DebugRoot> \\ <Module Name> \\ TIMEOUT**

donde *<DebugRoot>* es la ruta de acceso del Registro descrita en el tema Funciones de salida de [depuración](debug-output-functions.md).

Si la clave no existe, el valor predeterminado del tiempo de espera es INFINITE. Puede usar la función [**DbgSetWaitTimeout para**](dbgsetwaittimeout.md) invalidar la entrada del Registro.



| Función                                                       | Descripción                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Establece el valor de tiempo de espera de depuración.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Espera a que se señale a cualquiera (o a todos) de los objetos especificados. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Espera a que se señale un objeto.                         |



 

 

 



