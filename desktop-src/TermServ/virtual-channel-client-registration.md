---
title: Registro de cliente de canal virtual
description: Debe almacenar el nombre del archivo DLL de cliente en el registro.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792070"
---
# <a name="virtual-channel-client-registration"></a>Registro de cliente de canal virtual

Debe almacenar el nombre del archivo DLL de cliente en el registro.

En el registro, agregue una subclave a una de las siguientes ubicaciones:

**HKEY \_ Software de \_ usuario actual** \\  \\  \\  \\  \\ **Complementos** predeterminados de cliente de Microsoft Terminal Server

**HKEY \_ Software de \_ usuario actual** \\  \\  \\  \\  \\ **Complementos** de conexión de cliente de Microsoft Terminal Server

> [!Note]  
> En la ruta de acceso del registro, *Connection* representa el nombre de una conexión en el administrador de conexiones.

 

Las entradas de la clave **\\ \\ AddIns predeterminada** se aplican a todas las conexiones. Las entradas de la clave **\\  \\ AddIns de conexión** solo se aplican a la conexión identificada por la *conexión*. Las conexiones se pueden crear y administrar mediante el administrador de conexiones.

A la subclave se le puede asignar cualquier nombre. Debe contener un valor de **reg \_ SZ** o **reg \_ Expand \_ SZ** y puede contener opcionalmente un valor de **reg \_ DWORD** . La sintaxis de los valores de **reg \_ SZ** o **reg \_ Expand \_** es como se indica a continuación.

``` syntax
Name = DLLname
```

Si **Name** es un valor de **reg \_ Expandable \_** , puede contener variables de entorno no expandidas que se expandan en tiempo de ejecución.

El valor de *DLLname* puede ser una ruta de acceso completa. Si *DLLname* no contiene una ruta de acceso, se usa la estrategia de búsqueda dll estándar. Para obtener más información, vea la sección Comentarios para [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 