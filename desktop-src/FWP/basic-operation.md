---
title: Operación de WFP
description: La plataforma de filtrado de Windows (WFP) realiza sus tareas mediante la integración de las siguientes capas básicas de entidades, filtros, correcciones de compatibilidad y llamadas.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e7a7d38bd0de5b1f549e2187c414644bf68442
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665815"
---
# <a name="wfp-operation"></a>Operación de WFP

La plataforma de filtrado de Windows (WFP) realiza sus tareas mediante la integración de las siguientes entidades básicas: *capas*, *filtros*, *correcciones de compatibilidad* y *llamadas*.

## <a name="layers"></a>Capas

Una *capa* es un contenedor administrado por el motor de filtro cuya función es organizar los filtros en conjuntos. Una capa no es un módulo de la pila de red. Cada capa tiene un esquema que define el tipo de filtros que se pueden agregar a él. Consulte [condiciones de filtrado disponibles en cada capa de filtrado](filtering-conditions-available-at-each-filtering-layer.md) para obtener más información.

Las capas pueden contener subcapas para administrar los requisitos de filtro en conflicto, como "bloquear puertos TCP por encima de 1024" y "abrir el puerto 1080". Las reglas para administrar conflictos de filtrado se determinan mediante el [arbitraje de filtros](filter-arbitration.md).

WFP contiene un conjunto de [subcapas integradas](management-filtering-sublayer-identifiers.md). Cada capa hereda todas las subcapas integradas. Los usuarios también pueden agregar sus propias subcapas.

La lista de capas del motor de filtros se proporciona en la sección de referencia de los [**identificadores de capas de filtrado**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtros

Un *filtro* es una regla que se compara con los paquetes entrantes o salientes. La regla indica al motor de filtrado qué hacer con el paquete, incluido para llamar a un módulo de llamada para la inspección profunda de paquetes o secuencias. Por ejemplo, un filtro puede especificar "bloquear el tráfico con un puerto TCP mayor que 1024" o "llamar a IDENTIFICADOres para todo el tráfico que no está protegido".

Un filtro en tiempo de arranque es un filtro que se aplica en el momento del arranque en cuanto se inicia el controlador de pila TCP/IP (tcpip.sys). Se deshabilita un filtro de tiempo de arranque cuando se inicia BFE. Un filtro se marca como de tiempo de arranque mediante el establecimiento de la marca de [**filtro FWPM de \_ \_ \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) cuando se invoca [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) .

Un filtro en tiempo de ejecución es un filtro que se aplica después de que se inicia BFE. Un filtro en tiempo de ejecución puede ser estático, dinámico o persistente en función de la forma en que se creó. Vea [Administración de objetos](object-management.md) para obtener más información sobre los diferentes tipos de filtros en tiempo de ejecución y su duración.

## <a name="shims"></a>Correcciones

Una *corrección de compatibilidad (Shim* ) es un componente de modo kernel que toma decisiones de filtrado mediante la clasificación de las capas del motor de filtro. Cada corrección de compatibilidad se clasifica en una o más capas. Por ejemplo, la corrección de compatibilidad del módulo de capa de transporte se clasifica en la capa de transporte de entrada, la capa de transporte de salida y los niveles de conexión y Receive-Accept ALE para el primer paquete de un flujo.

A medida que los paquetes, los flujos y los eventos atraviesan la pila de red, las correcciones de compatibilidad las analizan para extraer las condiciones y los valores clasificables y, a continuación, se llama al motor de filtro para evaluarlos con respecto a los filtros de una capa determinada. El motor de filtro puede invocar una o varias llamadas como parte de la clasificación. Las correcciones de compatibilidad (shim) realizan la eliminación real de paquetes, secuencias y eventos según el resultado de la clasificación realizada por el motor de filtro.

## <a name="callouts"></a>Llamadas

Una *llamada* es un conjunto de funciones expuestas por un controlador y que se usa para el filtrado especializado. Se usan para realizar el análisis y la manipulación de los paquetes, como el examen de virus, los controles parentales examinan el contenido inadecuado, el análisis de los datos de paquetes para las herramientas de supervisión. Algunas llamadas, como el controlador de traducción de direcciones de red (NAT), están integradas en el sistema operativo. Otros fabricantes de software independientes (ISV) pueden proporcionar otras personas, como una llamada de control parental de HTTP o la llamada del sistema de detección de intrusiones (IDS). El motor de filtro invoca las funciones de llamada cuando se hace coincidir un filtro de llamada correspondiente en un nivel determinado.

Las llamadas se pueden registrar en cualquiera de las capas de WFP de modo kernel. Las llamadas pueden devolver una acción ("bloquear", "permitir" y, al realizar la inspección de la secuencia, "aplazar", "necesitar más datos", "quitar conexión") y puede modificar y proteger el tráfico de red entrante y saliente.

Una vez que se registra una llamada con el motor de filtro, puede recibir el tráfico de red que se va a procesar. El tráfico puede ser paquetes, secuencias o eventos en función de la capa. Un agente de aplicación o firewall hace que el tráfico se pase a una llamada agregando un filtro cuya acción es "callout" y cuyo identificador de llamada es el identificador de la llamada. Las llamadas pueden indicar al motor de filtro que devuelva "bloquear" o "permitir" a la corrección de compatibilidad. Las llamadas también pueden devolver "Continue" para permitir que otros filtros procesen el paquete.

Un controlador de llamada puede exponer varias llamadas.

Una llamada debe agregarse (con [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) y registrarse (con [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) antes de que se pueda usar. Se requiere una llamada a **FwpmCalloutAdd0** antes de la creación de filtros que hacen referencia a la llamada. Se requiere una llamada a FwpsCalloutRegister para que WFP pueda invocar la llamada cuando se encuentren coincidencias con los filtros de llamada. De forma predeterminada, los filtros que hacen referencia a llamadas que se han agregado pero que todavía no se han registrado con el motor de filtro se tratan como filtros de "bloque". No importa el orden de llamar a **FwpmCalloutAdd0** y FwpsCalloutRegister. Una llamada persistente debe agregarse una sola vez y debe registrarse cada vez que se inicie el controlador que implementa la llamada (por ejemplo, después de un reinicio).

## <a name="classification"></a>Clasificación

La clasificación es el proceso de aplicar filtros al tráfico de red (paquete, secuencia o evento) con el fin de determinar el resultado de "permitir" o "bloquear" para ese tráfico. Para un paquete, secuencia o evento hay una llamada de clasificación por nivel.

Durante la clasificación, las propiedades (por ejemplo, la dirección de origen) del paquete, la secuencia o el evento se comparan con las condiciones de filtro establecidas en los filtros de la capa en la que se invoca la clasificación. Cuando se encuentran coincidencias, se usa el algoritmo de [arbitraje de filtro](filter-arbitration.md) para determinar el resultado del proceso de clasificación.

Un Shim desencadena una solicitud de clasificación.

Las acciones de clasificación pueden ser:

-   Permitir
-   Bloquear
-   Llamada
    -   Permitir
    -   Bloquear
    -   Continuar
    -   Acepta
    -   Necesita más datos
    -   Quitar conexión

## <a name="wfp-operation"></a>Operación de WFP

En el momento del arranque, en cuanto se inicia el controlador de pila TCP/IP (tcpip.sys), el motor de filtro de modo kernel aplica la Directiva de seguridad del sistema a través de filtros en tiempo de arranque.

Una vez que el motor de filtrado de base (BFE) se inicia en modo de usuario, los filtros persistentes se agregan a la plataforma, se deshabilitan los filtros de tiempo de arranque y se envían notificaciones a los controladores de llamadas que se suscribieron mediante [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). Las notificaciones se envían inmediatamente después de que se complete la inicialización de BFE. La plataforma ahora está lista para que se registren las llamadas y para que se agreguen los objetos en tiempo de ejecución.

La transición desde el tiempo de arranque a los filtros persistentes puede ser de varios segundos o incluso más en un equipo lento. Es atómico, por lo que si un proveedor tiene un filtro persistente y un tiempo de arranque, nunca habrá una ventana cuando no haya ninguna en vigor.

Una vez iniciado BFE, los agentes de Firewall pueden agregar filtros en tiempo de ejecución o soluciones de Firewall personalizadas. BFE procesa estos filtros y los envía a la capa del motor de filtros adecuada para su cumplimiento. BFE también acepta la configuración de autenticación y envía esta configuración a los módulos de creación de claves IPsec (IKE/AuthIP). Consulte [configuración de IPSec](ipsec-configuration.md) para obtener más información.

En cualquier momento, los filtros y la configuración de autenticación se pueden agregar, quitar o cambiar en el sistema a través de la interfaz RPC expuesta por BFE. También se pueden agregar o quitar subcapas y módulos de llamada.

Flujo de datos:

1.  Un paquete entra en la pila de red.
2.  La pila de red busca y llama a una corrección de compatibilidad.
3.  La corrección de compatibilidad invoca el proceso de clasificación en una capa determinada.
4.  Durante la clasificación, se buscan coincidencias con los filtros y se realiza la acción resultante. (Consulte [arbitraje de filtros](filter-arbitration.md)).
5.  Si los filtros de llamada coinciden durante el proceso de clasificación, se invocan las llamadas correspondientes.
6.  La corrección de compatibilidad (shim) actúa en la decisión de filtrado final (por ejemplo, quitar el paquete).

El flujo de datos de salida sigue un patrón similar.

En los temas siguientes se describe con más detalle el funcionamiento de WFP.

-   [Flujos de paquetes TCP](tcp-packet-flows.md)
-   [Flujos de paquetes UDP](udp-packet-flows.md)
-   [Arbitraje de filtro](filter-arbitration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos](object-model.md)
</dt> <dt>

[Administración de objetos](object-management.md)
</dt> </dl>

 

 