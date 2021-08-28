---
description: Funciones de depuración de espera
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funciones de depuración de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2aabec60a14ff36d74298a21d31c91b4bc6d94
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884024"
---
# <a name="wait-debugging-functions"></a>Funciones de depuración de espera

Microsoft DirectShow proporciona varias funciones para depurar esperas infinitas.

En las compilaciones comerciales, las funciones [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) y [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionan como sus homólogos de api de Windows, **WaitForMultipleObjects** y **WaitForSingleObject,** con intervalos de tiempo de espera infinitos.

En las compilaciones de depuración, estas funciones usan un valor de tiempo de espera global. Si expira el tiempo de espera, la función desencadena una aserción. La siguiente clave del Registro especifica el valor de tiempo de espera, en milisegundos:

**HKEY \_ LOCAL \_ MACHINE \\ &lt; DebugRoot &gt; \\ <Module Name> \\ TIMEOUT**

donde *&lt; DebugRoot es la &gt;* ruta de acceso del Registro descrita en el tema Funciones de salida de [depuración](debug-output-functions.md).

Si la clave no existe, el valor predeterminado del tiempo de espera es INFINITE. Puede usar la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para invalidar la entrada del Registro.



| Función                                                       | Descripción                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Establece el valor de tiempo de espera de depuración.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Espera a que se señale cualquier (o todos) de los objetos especificados. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Espera a que se señale un objeto.                         |



 

 

 



