---
title: Implementar un sistema distribuido
description: Una manera de implementar software en un sistema distribuido es usar la compatibilidad con redes sin procesar.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab45f8175e82bdd1f5d6e49f3d94578473ed5c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903295"
---
# <a name="implementing-a-distributed-system"></a>Implementar un sistema distribuido

Una manera de implementar software en un sistema distribuido es usar la compatibilidad con redes sin procesar. Este enfoque incluye sockets, canalizaciones con nombre o publicaciones HTTP, se obtiene, etc. Todos estos modelos obligan al desarrollador a usar primitivas de programación de bajo nivel, de una forma u otra, que obligan al desarrollador a tratar con la representación de datos de red (NDR), a empaquetar datos, a administrar el tráfico de red y a las condiciones de error, la protección de integridad de datos y el cifrado, etc.

RPC ofrece un modelo de programación en el que el desarrollador conserva el control granular de la interacción de red entre el cliente y el servidor a través de una API enriquecida, al tiempo que se ahorra a los desarrolladores de los detalles y las cargas que un sistema distribuido tiende a introducir.

Por ejemplo, considere la carga asociada a varios enfoques para proteger la integridad y la privacidad de los intercambios de mensajes en un sistema distribuido. Al considerar la seguridad de la red para los intercambios de paquetes, algunas protecciones son más débiles, algo más seguras. No hay ninguna seguridad de red verdadera, solo varios mecanismos de seguridad basados en paquetes; seguridad que identifica al autor de la llamada (que tiende a ser débil también, ya que el contenido de los paquetes a menudo se puede cambiar en tránsito), seguridad que protege la integridad del paquete sin proteger su privacidad (varias firmas y hashes) y seguridad que protege la privacidad del intercambio de mensajes (varios mecanismos de cifrado).

Otra carga de la implementación de un sistema distribuido seguro son los algoritmos necesarios para implementar primitivas de seguridad como el cifrado, la firma, la autenticación, etc. Un desarrollador puede implementar esos algoritmos, pero hacerlo es difícil, propenso a errores e incluso arriesgado, ya que los algoritmos resultantes suelen tener problemas de seguridad sutiles. Como alternativa, un programador puede utilizar un proveedor de seguridad disponible para implementar la protección de las interacciones de red en un sistema distribuido.

Con RPC, estas cargas se resuelven muy fácilmente. Un programador simplemente debe indicar a RPC qué paquete de seguridad se debe usar y qué protección de seguridad se debe aplicar al intercambio de mensajes (en términos de autenticación, cifrado, autenticación mutua, seguimiento de identidad del llamador, etc.). RPC se ocupa de todos los detalles en segundo plano de forma eficaz, pero proporciona al desarrollador control total sobre la manera de proteger los datos con precisión.

 

 




