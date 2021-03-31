---
description: La agrupación de objetos es un servicio automático proporcionado por COM+ que le permite configurar un componente para que las instancias de se mantengan activas en un grupo, listas para ser utilizadas por cualquier cliente que solicite el componente.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Conceptos de agrupación de objetos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb2aa6481b2493371801d0d274420d356b0a32e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423283"
---
# <a name="com-object-pooling-concepts"></a>Conceptos de agrupación de objetos COM+

La agrupación de objetos es un servicio automático proporcionado por COM+ que le permite configurar un componente para que las instancias de se mantengan activas en un grupo, listas para ser utilizadas por cualquier cliente que solicite el componente. Puede configurar y supervisar de forma administrativa el grupo mantenido para un componente determinado, especificando características como el tamaño del grupo y los valores de tiempo de espera de la solicitud de creación. Cuando la aplicación se está ejecutando, COM+ administra el grupo y controla los detalles de la activación y reutilización de objetos de acuerdo con los criterios especificados.

Puede lograr ventajas muy significativas en el rendimiento y el escalado mediante la reutilización de objetos de esta manera, especialmente cuando se escriben para sacar el máximo partido de la reutilización. Con la agrupación de objetos, obtendrá las siguientes ventajas:

-   Puede acelerar el tiempo de uso de los objetos para cada cliente, Factorizando la inicialización de recursos y la inicialización lenta del trabajo real que el objeto realiza para los clientes.
-   Puede compartir el costo de adquirir recursos caros en todos los clientes.
-   Puede preasignar objetos cuando se inicia la aplicación, antes de que entren las solicitudes de cliente.
-   Puede controlar el uso de recursos con la administración de grupos administrativos; por ejemplo, si establece un nivel de grupo máximo adecuado, puede mantener abierto solo todas las conexiones de base de datos para las que tiene una licencia.
-   Puede configurar la agrupación de forma administrativa para aprovechar las ventajas de los recursos de hardware disponibles, lo que le permite ajustar fácilmente la configuración del grupo cuando cambien los recursos de hardware disponibles.
-   Puede acelerar el tiempo de reactivación de los objetos que usan la [activación Just-in-Time (JIT)](com--just-in-time-activation.md), y controlar deliberadamente cómo se dedican los recursos a los clientes.

## <a name="writing-poolable-objects"></a>Escribir objetos agrupables

Los objetos agrupables deben cumplir ciertos requisitos para permitir que varios clientes puedan usar una única instancia de objeto. Por ejemplo, no pueden mantener el estado del cliente ni tener ninguna afinidad de subprocesos. Los objetos transaccionales también tienen requisitos concretos, en los que los recursos administrados mantenidos por un objeto agrupado se deben dar de alta manualmente en una transacción.

Los objetos agrupados pueden implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) para controlar cómo se reutilizan. Esto les permite realizar la inicialización cuando se activa en un contexto determinado, limpiar cualquier estado de cliente durante la desactivación e indicar cuándo se encuentran en un estado no reutilizable.

A menudo, resulta útil escribir objetos agrupables de una manera bastante genérica para que se puedan personalizar administrativamente con una cadena de constructor. Por ejemplo, se puede escribir un objeto para que contenga una conexión ODBC genérica, con un determinado DSN especificado administrativamente en una cadena de constructor.

En los temas de esta sección, que se describen en la tabla siguiente, se proporciona información sobre cómo funciona la agrupación de objetos en COM+, así como información sobre cómo escribir, configurar e implementar objetos agrupables.



| Tema                                                                                                 | Descripción                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Cómo funciona la agrupación de objetos](how-object-pooling-works.md)<br/>                                   | Presenta los conceptos básicos.<br/>                                                                      |
| [Mejorar el rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)<br/> | Proporciona detalles específicos sobre cómo se puede usar la agrupación de objetos de forma más eficaz.<br/>                 |
| [Requisitos para objetos agrupables](requirements-for-poolable-objects.md)<br/>                 | Proporciona detalles sobre cómo escribir un objeto que se va a agrupar.<br/>                              |
| [Agrupar objetos transaccionales](pooling-transactional-objects.md)<br/>                         | Proporciona detalles sobre los requisitos especiales que se aplican a los objetos transaccionales agrupables.<br/> |
| [Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)<br/>         | Describe cómo se pueden implementar objetos agrupados para controlar cómo se reutilizan.<br/>               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de agrupación de objetos COM+](com--object-pooling-tasks.md)
</dt> </dl>

 

 




