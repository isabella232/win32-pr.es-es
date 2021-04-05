---
description: Una tabla de enrutamiento distribuida (DRT) existe como una malla de nodos cooperativos, donde cada nodo es una instancia de una aplicación que usa la API de DRT.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Acerca de las tablas de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfca9f81cc609d97584ef5a11f999722c696858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909801"
---
# <a name="about-distributed-routing-tables"></a>Acerca de las tablas de enrutamiento distribuido

Una tabla de enrutamiento distribuida (DRT) existe como una malla de nodos cooperativos, donde cada nodo es una instancia de una aplicación que usa la API de DRT. Los nodos que publican claves son responsables de ayudar a otros nodos a publicar y resolver claves. Los nodos también pueden participar en un modo de "resolver solo", que no les exige que ayuden a los compañeros. El protocolo DRT se ejecuta a través de un transporte UDP/IPv6.

Un nodo que publica una clave genera y mantiene una tabla de enrutamiento local de otros nodos en la malla. Esta tabla de enrutamiento está optimizada para que el nodo pueda localizar rápidamente una clave específica de la malla mediante la búsqueda de la clave directamente en la tabla de enrutamiento local o mediante la petición de otras claves de publicación de nodos que se acerquen numéricamente al destino. Esta acción se repite hasta que se encuentra la clave requerida o hasta que el nodo determina que no existe esa clave.

Las claves de DRT son enteros de 256 bits sin signo. La proximidad entre las claves se define por la diferencia numérica entre ellas. El espacio de DRT se considera circular. Por ejemplo, el primer valor de clave posible y el último valor de clave posible se consideran vecinos.

En un DRT seguro, se necesitan nodos para autenticar las claves que publican. El mecanismo por el que los nodos autentican las claves deben establecerse mediante la API de DRT cuando se inicializa la DRT. Esto se realiza mediante la elección de un proveedor de seguridad para DRT. Un proveedor de seguridad es un módulo que puede generar tokens que se usan para autenticar claves y comprobar los tokens generados por otros nodos. Debe implementar la interfaz del proveedor de seguridad que se define en esta documentación. La DRT de Windows 7 se suministra con dos proveedores de seguridad totalmente implementados que se pueden usar para compilar aplicaciones de Windows.

Durante la inicialización, una aplicación también debe proporcionar el DRT con un proveedor de arranque. El proveedor de bootstrap es un módulo que puede recuperar los puntos de conexión de red de los nodos que ya están presentes en la malla de DRT y al que se llama cuando se establece un nuevo nodo. Al igual que el módulo de proveedor de seguridad, el proveedor de arranque debe implementar una interfaz bien definida. La DRT de Windows 7 se suministra con dos proveedores de bootstrap totalmente implementados.

La DRT tiene en cuenta los vecinos inmediatos de una clave especial. Las cinco claves más pequeñas numéricamente menores y las cinco claves más cercanas numéricamente mayores que una clave publicada forman lo que se denomina conjunto de hojas. DRT informa de los cambios en el conjunto de hojas de una clave a través de la API de DRT.

## <a name="drt-life-cycle-and-state-transitions"></a>Ciclo de vida de DRT y transiciones de estado

Una aplicación puede inicializar una instancia de DRT local mediante la función [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen) . Esta función desencadena el proceso de arranque, donde la API de DRT llama a en el proveedor de bootstrap para conocer las claves y los puntos de conexión de red de otros nodos que ya participan en el DRT. Si el proveedor de arranque localiza correctamente al menos otro nodo, el DRT entra en el \_ estado activo de DRT. En este estado, la aplicación puede buscar claves publicadas por otros nodos y puede publicar claves que se puedan resolver. Si el proveedor de arranque no puede localizar otros nodos correctamente, el DRT entra en el \_ Estado independiente de DRT. La DRT permanecerá en el \_ Estado independiente de DRT e intentará iniciarse de forma periódica para buscar elementos del mismo nivel y pasar al \_ estado activo de DRT.

Un nodo puede pasar a estos Estados desde DRT \_ activo.

| Estado del ciclo de vida | Condiciones                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_solo DRT       | El nodo local no ha detectado otros nodos en la DRT. Mientras se encuentra en este estado, el nodo continúa escuchando otros nodos dentro de DRT.<br/> Si otro nodo se une a DRT, el nodo local pasará al \_ estado activo de DRT. Si la red está inactiva, pasará a DRT \_ no \_ Network. En caso de que se produzca un error grave con la DRT, el nodo pasará al \_ Estado de error de DRT.<br/> |
| DRT \_ sin \_ red | Cuando un nodo pierde la conectividad de red, pasa al estado de \_ no \_ red de DRT. En este momento, la aplicación puede esperar a que se restaure la conectividad de red y puede cerrar la DRT.<br/>                                                                                                                                                                                                                    |
| error de DRT \_     | Se ha producido un error grave dentro del nodo local. Por ejemplo, si el equipo local se queda sin memoria física.<br/> Mientras un nodo entra en este estado, la aplicación debe llamar a la API [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) , corregir el problema y volver a inicializar la DRT con [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).<br/>                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Table API de enrutamiento distribuido](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




