---
description: Registrar y anular el registro de claves
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrar y anular el registro de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668060"
---
# <a name="registering-and-deregistering-keys"></a>Registrar y anular el registro de claves

## <a name="registering-keys"></a>Registrar claves

Un nodo puede registrar claves con [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) en cualquier momento mientras se encuentra en el estado de DRT **\_ activo**, **DRT \_ solo** y DRT sin Estados de **\_ \_ red** . Claves registradas **solo \_ en DRT** y DRT no solo los Estados de **\_ \_ red** pueden ser reconocidos por otros DRTs después de que el nodo local haya pasado a **DRT \_ activo**.

No se pueden registrar claves idénticas dentro de la misma instancia de DRT cuando se usa [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Si se intenta registrar claves idénticas, se producirá un error en el registro de la segunda clave. El uso de claves idénticas también debe evitarse entre diferentes instancias de DRT. Busca en la designación de clave única estas claves compartidas idénticas podrían devolver cualquiera de las claves, independientemente de los datos que estén asociados a la clave.

> [!Note]  
> Si se requiere un comportamiento diferente para la implementación, se puede crear un proveedor de seguridad en lugar de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) para acomodar.

 

## <a name="deregistering-keys"></a>Anular el registro de claves

Un nodo puede anular el registro de una clave en cualquier momento después de que se haya registrado. Sin embargo, solo la aplicación que registró la clave puede anular su registro. Una aplicación puede anular el registro de una clave del nodo local mediante la función [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) . Una vez finalizada la función, desencadena un evento de **\_ \_ \_ \_ cambio de clave LEAFSET de evento de DRT** , que informa a la aplicación así como a otros nodos que participan en la malla de DRT.

En el estado **de \_ error de DRT** , la llamada necesaria de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) producirá la eliminación del registro de todas las claves de la infraestructura de DRT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar una tabla de enrutamiento distribuida](searching-a-distributed-routing-table.md)
</dt> <dt>

[Acerca de las tablas de enrutamiento distribuido](about-distributed-routing-tables.md)
</dt> <dt>

[Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



