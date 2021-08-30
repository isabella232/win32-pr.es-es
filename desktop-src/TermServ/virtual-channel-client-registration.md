---
title: Registro de cliente de canal virtual
description: Debe almacenar el nombre del archivo DLL de cliente en el Registro.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac019a2c32a1eed09eb11b45a73261f1510bfa409ebe8e049370023f9199ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868655"
---
# <a name="virtual-channel-client-registration"></a>Registro de cliente de canal virtual

Debe almacenar el nombre del archivo DLL de cliente en el Registro.

En el Registro, agregue una subclave a una de las siguientes ubicaciones:

**HKEY \_ Complementos \_ predeterminados de** cliente de \\  \\ **Microsoft** \\ **Terminal Server** \\ **de** \\  SOFTWARE DE USUARIO ACTUAL

**HKEY \_ Complementos \_ de conexión** de cliente de \\  \\ **Microsoft** \\ **Terminal Server de** \\  \\  SOFTWARE ACTUAL

> [!Note]  
> En la ruta de acceso del Registro, *connection* representa el nombre de una conexión en Connection Manager.

 

Las entradas de la **\\ clave Complementos predeterminados \\ se** aplican a todas las conexiones. Las entradas de la **\\** _clave_*_\\ addins de_* conexión solo se aplican a la conexión identificada por la *conexión*. Las conexiones se pueden crear y administrar mediante Connection Manager.

A la subclave se le puede dar cualquier nombre. Debe contener un valor **REG \_ SZ** o **REG EXPAND \_ \_ SZ** y, opcionalmente, puede contener un **valor REG \_ DWORD.** La sintaxis del **valor REG \_ SZ** **o REG EXPAND \_ \_ SZ** es la siguiente.

``` syntax
Name = DLLname
```

Si **Name** es un **valor REG EXPAND \_ \_ SZ,** puede contener variables de entorno no exploradas que se expanden en tiempo de ejecución.

El valor de *DLLname* puede ser una ruta de acceso completa. Si *DLLname* no contiene una ruta de acceso, se usa la estrategia de búsqueda dll estándar. Para obtener más información, vea la sección Comentarios de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 