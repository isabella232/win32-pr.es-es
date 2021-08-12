---
description: Registro y anulación del registro de claves
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registro y anulación del registro de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d586fc2bf399a30b8a962611a21a4e0994d88f4513453c071b110de1d4142b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612168"
---
# <a name="registering-and-deregistering-keys"></a>Registro y anulación del registro de claves

## <a name="registering-keys"></a>Registro de claves

Un nodo puede registrar claves con [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) en cualquier momento mientras se encuentra en los estados **DRT \_ ACTIVE**, **DRT \_ ALONE** y **DRT \_ NO \_ NETWORK.** Las claves registradas en los estados **DRT \_ ALONE** y **DRT \_ NO \_ NETWORK** solo pueden ser reconocidas por otros DRT después de que el nodo local haya pasado a **DRT \_ ACTIVE**.

No se pueden registrar claves idénticas dentro de la misma instancia de DRT cuando se [**usa DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Si se intenta registrar claves idénticas, se producirá un error en el registro de la segunda clave. También se debe evitar el uso de claves idénticas entre diferentes instancias de DRT. Las búsquedas en la designación de clave única que comparten estas claves idénticas podrían devolver cualquiera de las claves, independientemente de los datos asociados a la clave.

> [!Note]  
> Si se requiere un comportamiento diferente para la implementación, se puede crear un proveedor de seguridad en lugar de [**DrtCreateDerivedKeySecurityProvider para**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) dar cabida.

 

## <a name="deregistering-keys"></a>Anulación del registro de claves

Un nodo puede anular el registro de una clave en cualquier momento después de que se haya registrado. Sin embargo, solo la aplicación que registró la clave puede anular su registro. Una aplicación puede anular el registro de una clave del nodo local mediante la [**función DrtUnregisterKey.**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) Al finalizar, la función desencadena un evento **DRT \_ EVENT \_ LEAFSET \_ KEY \_ CHANGE,** que informa a la aplicación, así como a otros nodos que participan en la malla de DRT.

Mientras se encuentra en **el estado DRT \_ FAULTED,** la llamada necesaria de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) dará lugar a que la infraestructura de DRT anulará el registro de todas las claves.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda de una tabla de enrutamiento distribuido](searching-a-distributed-routing-table.md)
</dt> <dt>

[Acerca de las tablas de enrutamiento distribuido](about-distributed-routing-tables.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



