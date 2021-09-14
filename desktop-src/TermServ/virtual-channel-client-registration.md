---
title: Registro de cliente de canal virtual
description: Debe almacenar el nombre del archivo DLL de cliente en el Registro.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249843"
---
# <a name="virtual-channel-client-registration"></a>Registro de cliente de canal virtual

Debe almacenar el nombre del archivo DLL de cliente en el Registro.

En el Registro, agregue una subclave a una de las siguientes ubicaciones:

**HKEY \_ Current \_ USER** \\ **Software** \\ **Microsoft** Terminal Server \\ **Client** \\ **Default** \\ **Addins**

**HKEY \_ CURRENT \_ USER** \\ **Software** Microsoft Terminal Server Client \\  \\  \\ **connection** \\ **Addins** (Complementos de conexión de cliente de Microsoft Terminal Server de SOFTWARE ACTUAL)

> [!Note]  
> En la ruta de acceso del Registro, *la* conexión representa el nombre de una conexión en Connection Manager.

 

Las entradas de la **\\ clave Complementos predeterminados \\ se** aplican a todas las conexiones. Las entradas de la **\\** _clave_*_\\ de complementos de conexión_* solo se aplican a la conexión identificada por la *conexión*. Las conexiones se pueden crear y administrar mediante Connection Manager.

A la subclave se le puede dar cualquier nombre. Debe contener un valor **REG \_ SZ** o **REG EXPAND \_ \_ SZ** y, opcionalmente, puede contener un **valor REG \_ DWORD.** La sintaxis del **valor \_ REG SZ** o REG EXPAND **\_ \_ SZ** es la siguiente.

``` syntax
Name = DLLname
```

Si **Name** es un **valor REG EXPAND \_ \_ SZ,** puede contener variables de entorno no exploradas que se expanden en tiempo de ejecución.

El valor de *DLLname* puede ser una ruta de acceso completa. Si *DLLname* no contiene una ruta de acceso, se usa la estrategia de búsqueda dll estándar. Para obtener más información, vea la sección Comentarios de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 