---
title: Operación WFP
description: Windows Plataforma de filtrado (WFP) realiza sus tareas mediante la integración de las siguientes entidades básicas Capas, Filtros, Correcciones de compatibilidad (Shim) y Llamadas.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254ed468b856392477a643ce13f2b609245031f7363865b8c93ccfda64ba9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015393"
---
# <a name="wfp-operation"></a>Operación WFP

Windows La plataforma de filtrado (WFP) realiza sus tareas mediante la integración de las siguientes entidades *básicas:* *Capas* *,* Filtros, Correcciones de compatibilidad *(Shim)* y Llamadas .

## <a name="layers"></a>Capas

Una *capa* es un contenedor administrado por el motor de filtros cuya función es organizar los filtros en conjuntos. Una capa no es un módulo de la pila de red. Cada capa tiene un esquema que define el tipo de filtros que se pueden agregar a ella. Consulte [Condiciones de filtrado disponibles en cada capa de filtrado](filtering-conditions-available-at-each-filtering-layer.md) para obtener más información.

Las capas pueden contener sub capas para administrar los requisitos de filtro en conflicto, como "Bloquear puertos TCP por encima de 1024" y "Abrir puerto 1080". Las reglas para administrar conflictos de filtrado se determinan mediante [filter arbitration](filter-arbitration.md).

WFP contiene un conjunto [de sub capas integradas.](management-filtering-sublayer-identifiers.md) Cada capa hereda todas las subcapas integradas. Los usuarios también pueden agregar sus propias sub capas.

La lista de capas del motor de filtro se proporciona en el tema de la sección de referencia [**Identificadores de capa de filtrado**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtros

Un *filtro* es una regla que coincide con los paquetes entrantes o salientes. La regla indica al motor de filtrado qué hacer con el paquete, incluida la llamada a un módulo de llamada para la inspección profunda de paquetes o flujos. Por ejemplo, un filtro puede especificar "Bloquear el tráfico con un puerto TCP mayor que 1024" o "Llamar a IDS para todo el tráfico que no está protegido".

Un filtro en tiempo de arranque es un filtro que se aplica en tiempo de arranque en cuanto se inicia el controlador de pila TCP/IP (tcpip.sys). Un filtro en tiempo de arranque se deshabilita cuando se inicia BFE. Un filtro se marca como tiempo de arranque estableciendo la marca [**\_ FWPM FILTER \_ FLAG \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) cuando [**se invoca FwpmFilterAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Un filtro en tiempo de ejecución es un filtro que se aplica después de iniciar BFE. Un filtro en tiempo de ejecución puede ser estático, dinámico o persistente en función de la forma en que se creó. Consulte [Administración de objetos](object-management.md) para obtener más información sobre los distintos tipos de filtros en tiempo de ejecución y su duración.

## <a name="shims"></a>Cuñas

Una corrección de compatibilidad *(shim)* es un componente en modo kernel que toma decisiones de filtrado mediante la clasificación en las capas del motor de filtro. Cada corrección de compatibilidad (shim) se clasifica en una o varias capas. Por ejemplo, la corrección de compatibilidad (shim) del módulo de la capa de transporte se clasifica con respecto a la capa de transporte entrante, la capa de transporte saliente y las capas Conectar y Receive-Accept de ALE para el primer paquete de un flujo.

A medida que los paquetes, secuencias y eventos atraviesan la pila de red, las correcciones de compatibilidad (shim) los analizan para extraer las condiciones y los valores clasificables y, a continuación, llaman al motor de filtros para evaluarlos con los filtros de una capa determinada. El motor de filtros puede invocar una o varias llamadas como parte de la clasificación. Las correcciones de compatibilidad (shim) realizan la colocación real de paquetes, secuencias y eventos en función del resultado de la clasificación realizada por el motor de filtros.

## <a name="callouts"></a>Llamadas

Una *llamada es* un conjunto de funciones expuestas por un controlador y que se usan para el filtrado especializado. Se usan para realizar análisis y manipulación de los paquetes, como examen de virus, examen de controles parentales en busca de contenido inadecuado, análisis de datos de paquetes para herramientas de supervisión. Algunas llamadas, como el controlador de traducción de direcciones de red (NAT), están integradas en el sistema operativo. Otros, como una llamada de control parental HTTP o la llamada del Sistema de detección de intrusiones (IDS), pueden proporcionarse por proveedores de software independientes (ISV). El motor de filtros invoca las funciones de llamada cuando un filtro de llamada correspondiente coincide en una capa determinada.

Las llamadas se pueden registrar en cualquiera de las capas de WFP en modo kernel. Las llamadas pueden devolver una acción ("Bloquear", "Permitir" y, al realizar la inspección de flujos, "Aplazar", "Necesita más datos", "Quitar conexión") y puede modificar y proteger el tráfico de red entrante y saliente.

Una vez que se registra una llamada con el motor de filtro, puede recibir tráfico de red para procesar. El tráfico puede ser paquetes, flujos o eventos en función de la capa. Una aplicación o un agente de firewall hace que el tráfico se pase a una llamada agregando un filtro cuya acción es "Llamada" y cuyo identificador de llamada es el identificador de esa llamada. Las llamadas pueden indicar al motor de filtros que devuelva "Block" o "Permit" a la corrección de compatibilidad (shim). Las llamadas también pueden devolver "Continuar" para permitir que otros filtros procese el paquete.

Un controlador de llamada puede exponer varias llamadas.

Es necesario agregar una llamada (con [**FwpmCalloutAdd0)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)y registrarla (con [FwpsCalloutRegister)](/windows-hardware/drivers/ddi/_netvista/)para poder usarse. Se requiere una llamada **a FwpmCalloutAdd0** antes de la creación de filtros que hacen referencia a la llamada. Se requiere una llamada a FwpsCalloutRegister para que WFP pueda invocar la llamada cuando se coincidan los filtros de llamada. De forma predeterminada, los filtros que hacen referencia a las llamadas que se han agregado pero aún no se han registrado con el motor de filtros se tratan como filtros "Bloquear". El orden de llamar **a FwpmCalloutAdd0** y FwpsCalloutRegister no importa. Una llamada persistente debe agregarse una sola vez y debe registrarse cada vez que se inicie el controlador que implementa la llamada (por ejemplo, después de un reinicio).

## <a name="classification"></a>clasificación

La clasificación es el proceso de aplicar filtros al tráfico de red (paquete, flujo o evento) para determinar un resultado de "Permitir" o "Bloquear" para ese tráfico. Para un paquete, flujo o evento, hay una llamada de clasificación por capa.

Durante la clasificación, las propiedades (por ejemplo, la dirección de origen) del paquete, la secuencia o el evento se comparan con las condiciones de filtro establecidas en los filtros de la capa donde se invoca la clasificación. Cuando se encuentran coincidencias, [se usa el algoritmo Filter Arbitration](filter-arbitration.md) para determinar el resultado del proceso de clasificación.

Una corrección de compatibilidad (shim) desencadena una solicitud de clasificación.

Las acciones de clasificación pueden ser:

-   Permitir
-   Bloquear
-   Llamada
    -   Permitir
    -   Bloquear
    -   Continuar
    -   Aplazar
    -   Necesita más datos
    -   Quitar conexión

## <a name="wfp-operation"></a>Operación WFP

En tiempo de arranque, en cuanto se inicia el controlador de pila TCP/IP (tcpip.sys), el motor de filtro en modo kernel aplica la directiva de seguridad del sistema a través de filtros de tiempo de arranque.

Una vez que el motor de filtrado base (BFE) se inicia en modo de usuario, se agregan filtros persistentes a la plataforma, se deshabilitan los filtros en tiempo de arranque y se envían notificaciones a los controladores de llamada que se han suscrito mediante [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). Las notificaciones se envían inmediatamente después de que se complete la inicialización de BFE. La plataforma ya está lista para que se registren las llamadas y para agregar objetos en tiempo de ejecución.

La transición del tiempo de arranque a los filtros persistentes podría ser de varios segundos o incluso más en una máquina lenta. Es atómico, por lo que si un proveedor tiene un tiempo de arranque y un filtro persistente, nunca habrá una ventana cuando ninguno esté en vigor.

Una vez que se inicia BFE, los agentes de firewall o las soluciones de firewall personalizadas pueden agregar filtros en tiempo de ejecución. BFE procesa estos filtros y los envía a la capa del motor de filtro adecuada para su cumplimiento. BFE también acepta la configuración de autenticación y envía esta configuración a los módulos de clave IPsec (IKE/AuthIP). Consulte [Configuración de IPsec](ipsec-configuration.md) para obtener más información.

En cualquier momento, los filtros y la configuración de autenticación se pueden agregar, quitar o cambiar en el sistema a través de la interfaz RPC expuesta por el BFE. Las sub capas y los módulos de llamada también se pueden agregar o quitar.

Flujo de datos:

1.  Un paquete entra en la pila de red.
2.  La pila de red busca y llama a una corrección de compatibilidad (shim).
3.  La corrección de compatibilidad (shim) invoca el proceso de clasificación en una capa determinada.
4.  Durante la clasificación, se comparan los filtros y se toma la acción resultante. (Vea [Filter Arbitration](filter-arbitration.md)).)
5.  Si algún filtro de llamada coincide durante el proceso de clasificación, se invocan las llamadas correspondientes.
6.  La corrección de compatibilidad (shim) actúa en la decisión de filtrado final (por ejemplo, quitar el paquete).

El flujo de datos salientes sigue un patrón similar.

En los temas siguientes se describe aún más el funcionamiento del WFP.

-   [Flujos de paquetes TCP](tcp-packet-flows.md)
-   [Flujos de paquetes UDP](udp-packet-flows.md)
-   [Filtro de cláusulas de conciliación](filter-arbitration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos](object-model.md)
</dt> <dt>

[Administración de objetos](object-management.md)
</dt> </dl>

 

 