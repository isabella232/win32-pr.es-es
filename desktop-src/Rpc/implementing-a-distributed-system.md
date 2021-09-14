---
title: Implementar un sistema distribuido
description: Una manera de implementar software en un sistema distribuido es usar la compatibilidad con redes sin procesar.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab45f8175e82bdd1f5d6e49f3d94578473ed5c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244670"
---
# <a name="implementing-a-distributed-system"></a>Implementar un sistema distribuido

Una manera de implementar software en un sistema distribuido es usar la compatibilidad con redes sin procesar. Este enfoque incluye sockets, canalizaciones con nombre o TPV HTTP, GTE, entre otros. Todos estos modelos obligan al desarrollador a usar primitivas de programación de bajo nivel, de una manera u otra, que obligan al desarrollador a tratar con la representación de datos de red (RCE), empaquetar datos, administrar el tráfico de red y las condiciones de error, la protección y el cifrado de la integridad de los datos, y así sucesivamente.

RPC ofrece un modelo de programación en el que el desarrollador conserva un control granular de la interacción de red entre el cliente y el servidor a través de una API enriquez, a la vez que ahorra a los desarrolladores los detalles y las cargas que un sistema distribuido tiende a introducir.

Por ejemplo, considere la carga asociada a varios enfoques para proteger la integridad y privacidad de los intercambios de mensajes en un sistema distribuido. Al considerar la seguridad de red para intercambios de paquetes, algunas protecciones son más débiles, otras más seguras. No hay ninguna seguridad de red verdadera, solo varios mecanismos de seguridad basados en paquetes; seguridad que identifica al autor de la llamada (que tiende a ser débil también, ya que el contenido del paquete a menudo se puede cambiar en tránsito), la seguridad que protege la integridad del paquete sin proteger su privacidad (varias firmas y hashes) y la seguridad que protege la privacidad del intercambio de mensajes (varios mecanismos de cifrado).

Otra carga de implementar un sistema distribuido seguro son los algoritmos necesarios para implementar primitivas de seguridad como el cifrado, la firma, la autenticación, entre otros. Un desarrollador puede implementar esos algoritmos, pero hacerlo es difícil, propenso a errores e incluso arriesgado, ya que los algoritmos resultantes suelen tener sutiles errores de seguridad. Como alternativa, un desarrollador puede usar un proveedor de seguridad disponible para implementar la protección de las interacciones de red dentro de un sistema distribuido.

Con RPC, ambas cargas se resuelven muy fácilmente. Un desarrollador simplemente necesita decir a RPC qué paquete de seguridad usar y qué protección de seguridad se debe aplicar al intercambio de mensajes (en términos de autenticación, cifrado, autenticación mutua, seguimiento de identidades de llamador, entre otros). RPC se encarga de todos los detalles en segundo plano de una manera eficaz, pero proporciona al desarrollador control total sobre exactamente cómo se protegerán los datos.

 

 




