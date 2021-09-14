---
description: Existe una tabla de enrutamiento distribuido (DRT) como una malla de nodos de cooperación, donde cada nodo es una instancia de una aplicación que usa la API de DRT.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Acerca de las tablas de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfca9f81cc609d97584ef5a11f999722c696858
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171334"
---
# <a name="about-distributed-routing-tables"></a>Acerca de las tablas de enrutamiento distribuido

Existe una tabla de enrutamiento distribuido (DRT) como una malla de nodos de cooperación, donde cada nodo es una instancia de una aplicación que usa la API de DRT. Los nodos que publican claves son responsables de ayudar a otros nodos a publicar y resolver claves. Los nodos también pueden participar de forma "solo resolver", lo que no requiere que ayuden a los compañeros. El protocolo DRT se ejecuta a través de un transporte UDP/IPv6.

Un nodo que publica una clave compila y mantiene una tabla de enrutamiento local de otros nodos de la malla. Esta tabla de enrutamiento está optimizada para que el nodo pueda localizar rápidamente una clave específica en la malla mediante la búsqueda de la clave directamente en la tabla de enrutamiento local o mediante la pregunta de otros nodos que publican claves numéricamente cerca del destino. Esta acción se repite hasta que se encuentra la clave necesaria o el nodo determina que no existe dicha clave.

Las claves DRT son enteros de 256 bits sin signo. La proximidad entre las claves se define por la diferencia numérica entre ellas. El espacio de claves DRT se considera circular. Por ejemplo, el primer valor de clave posible y el último valor de clave posible se consideran vecinos.

En un DRT seguro, los nodos son necesarios para autenticar las claves que publican. El mecanismo por el que los nodos autentican las claves debe establecerse mediante la API de DRT cuando se inicializa el DRT. Para ello, elija un proveedor de seguridad para drt. Un proveedor de seguridad es un módulo que puede generar tokens que se usan para autenticar las claves y comprobar los tokens generados por otros nodos. Debe implementar la interfaz del proveedor de seguridad que se define en esta documentación. El Windows 7 DRT se suministra con dos proveedores de seguridad totalmente implementados que se pueden usar para compilar Windows aplicaciones.

Durante la inicialización, una aplicación también debe proporcionar al DRT un proveedor de arranque. El proveedor de arranque es un módulo que puede recuperar los puntos de conexión de red de los nodos que ya están presentes en la malla de DRT y que el DRT llama cuando se establece un nuevo nodo. Al igual que el módulo del proveedor de seguridad, el proveedor de arranque debe implementar una interfaz bien definida. El Windows 7 DRT se incluye con dos proveedores de arranque totalmente implementados.

Drt considera los vecinos inmediatos de una clave especial. Las cinco claves más cercanas numéricamente más pequeñas y las cinco claves más cercanas numéricamente mayores que una clave publicada forman lo que se denomina conjunto hoja. Drt notifica los cambios en el conjunto hoja de una clave a través de la API de DRT.

## <a name="drt-life-cycle-and-state-transitions"></a>Ciclo de vida de DRT y transiciones de estado

Una aplicación puede inicializar una instancia de DRT local mediante la [**función DrtOpen.**](/windows/desktop/api/drt/nf-drt-drtopen) Esta función desencadena el proceso de arranque, donde la API de DRT llama al proveedor de arranque para obtener información sobre las claves y los puntos de conexión de red de otros nodos que ya participan en el DRT. Si el proveedor de arranque encuentra correctamente al menos otro nodo, el DRT entra en el estado ACTIVO de \_ DRT. En este estado, la aplicación puede buscar claves publicadas por otros nodos y puede publicar claves que se puedan resolver. Si el proveedor de arranque no puede localizar correctamente otros nodos, el DRT entra en el estado DRT \_ ALONE. El DRT permanecerá en el estado DRT ALONE e intentará arrancar periódicamente con el fin de localizar los pares y pasar al estado \_ ACTIVO de \_ DRT.

Un nodo puede realizar la transición a estos estados desde DRT \_ ACTIVE.

| Estado del ciclo de vida | Condiciones                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SOLO \_ DRT       | El nodo local no ha detectado otros nodos en el DRT. Mientras se encuentra en este estado, el nodo sigue escuchando otros nodos dentro del DRT.<br/> Si otro nodo se une al DRT, el nodo local pasará al estado ACTIVO de \_ DRT. Si la red está fuera de servicio, pasará a DRT \_ NO \_ NETWORK. En caso de que se produjese un error grave con el DRT, el nodo pasará al estado DRT \_ FAULTED.<br/> |
| DRT \_ NO \_ NETWORK | Cuando un nodo pierde la conectividad de red, pasa al estado DRT \_ NO \_ NETWORK. En este momento, la aplicación puede esperar a que se restaure la conectividad de red y puede cerrar el DRT.<br/>                                                                                                                                                                                                                    |
| ERROR \_ DE DRT     | Se ha producido un error grave en el nodo local. Por ejemplo, si la máquina local se queda sin memoria física.<br/> Mientras un nodo entra en este estado, la aplicación debe llamar a la API [**DrtClose,**](/windows/desktop/api/drt/nf-drt-drtclose) corregir el problema y volver a inicializar el DRT [**con DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).<br/>                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del enrutamiento distribuido Table API](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




