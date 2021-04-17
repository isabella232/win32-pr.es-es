---
description: Funciones de depuración de espera
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funciones de depuración de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687162"
---
# <a name="wait-debugging-functions"></a>Funciones de depuración de espera

Microsoft DirectShow proporciona varias funciones para depurar las esperas infinitas.

En las compilaciones comerciales, las funciones [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) y [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionan como sus homólogos de la API de Windows, **WaitForMultipleObjects** y **WaitForSingleObject**, con intervalos de tiempo de espera infinitos.

En las compilaciones de depuración, estas funciones usan un valor de tiempo de espera global. Si se agota el tiempo de espera, la función desencadena una aserción. La siguiente clave del registro especifica el valor de tiempo de espera, en milisegundos:

**HKEY \_ local \_ Machine \\ <DebugRoot> \\ <Module Name> \\ timeout**

donde *<DebugRoot>* es la ruta de acceso del registro que se describe en el tema [depurar funciones de salida](debug-output-functions.md).

Si la clave no existe, el valor predeterminado del tiempo de espera es infinito. Puede usar la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para invalidar la entrada del registro.



| Función                                                       | Descripción                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Establece el valor de tiempo de espera de depuración.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Espera a que se señalen todos los objetos especificados (o todos). |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Espera a que se señale un objeto.                         |



 

 

 



