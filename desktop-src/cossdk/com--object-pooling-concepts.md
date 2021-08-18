---
description: La agrupación de objetos es un servicio automático proporcionado por COM+ que permite configurar un componente para que las instancias de sí mismo se mantienen activas en un grupo, listas para que las utilice cualquier cliente que solicite el componente.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Conceptos de agrupación de objetos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836dd6f29c2f0bd120843a1a93763d46cb51224966f255251f7e3bfb4c7fa66a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129147"
---
# <a name="com-object-pooling-concepts"></a>Conceptos de agrupación de objetos COM+

La agrupación de objetos es un servicio automático proporcionado por COM+ que permite configurar un componente para que las instancias de sí mismo se mantienen activas en un grupo, listas para que las utilice cualquier cliente que solicite el componente. Puede configurar y supervisar administrativamente el grupo mantenido para un componente determinado, especificando características como el tamaño del grupo y los valores de tiempo de espera de la solicitud de creación. Cuando se ejecuta la aplicación, COM+ administra el grupo de forma automática, controlando los detalles de la activación de objetos y reutilizando según los criterios especificados.

Puede lograr un rendimiento y ventajas de escalado muy significativos mediante la reutilización de objetos de esta manera, especialmente cuando se escriben para aprovechar al máximo la reutilización. Con la agrupación de objetos, obtendrá las siguientes ventajas:

-   Puede acelerar el tiempo de uso de objetos para cada cliente, factoriendo la inicialización y la adquisición de recursos que consumen mucho tiempo del trabajo real que el objeto realiza para los clientes.
-   Puede compartir el costo de adquirir recursos costosos en todos los clientes.
-   Puede asignar previamente objetos cuando se inicia la aplicación, antes de que lleguen las solicitudes de cliente.
-   Por ejemplo, puede regular el uso de recursos con la administración de grupos administrativos; si establece un nivel máximo de grupo adecuado, solo puede mantener abiertas tantas conexiones de base de datos como tenga una licencia para .
-   Puede configurar la agrupación de forma administrativa para aprovechar al máximo los recursos de hardware disponibles. Puede ajustar fácilmente la configuración del grupo a medida que cambien los recursos de hardware disponibles.
-   Puede acelerar el tiempo de reactivación de los objetos que usan la activación [Just-In-Time (JIT),](com--just-in-time-activation.md)al tiempo que controla deliberadamente cómo se dedican los recursos a los clientes.

## <a name="writing-poolable-objects"></a>Escribir objetos agrupables

Los objetos agrupables deben cumplir determinados requisitos para permitir que varios clientes utilicen una única instancia de objeto. Por ejemplo, no pueden contener el estado de cliente ni tener ninguna afinidad de subproceso. Los objetos transaccionales también tienen requisitos concretos, ya que los recursos administrados que contiene un objeto agrupado se deben dar de alta manualmente en una transacción.

Los objetos agrupados pueden implementar [**IObjectControl para**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) controlar cómo se reutilizan. Esto les permite realizar la inicialización cuando se activan en un contexto determinado, limpiar cualquier estado de cliente en la desactivación e indicar cuándo se encuentran en un estado no reutilizable.

A menudo, resulta útil escribir objetos agrupables de forma algo genérica para que se puedan personalizar administrativamente con una cadena de constructor. Por ejemplo, se podría escribir un objeto para contener una conexión ODBC genérica, con un DSN determinado especificado administrativamente en una cadena de constructor.

Los temas de esta sección, que se describen en la tabla siguiente, proporcionan información sobre cómo funciona la agrupación de objetos en COM+, así como información sobre cómo escribir, configurar e implementar objetos agrupables.



| Tema                                                                                                 | Descripción                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Funcionamiento de la agrupación de objetos](how-object-pooling-works.md)<br/>                                   | Presenta conceptos básicos.<br/>                                                                      |
| [Mejora del rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)<br/> | Proporciona detalles específicos sobre cómo puede usar la agrupación de objetos de forma más eficaz.<br/>                 |
| [Requisitos para objetos agrupables](requirements-for-poolable-objects.md)<br/>                 | Proporciona detalles sobre cómo escribir un objeto que se va a agrupar.<br/>                              |
| [Agrupación de objetos transaccionales](pooling-transactional-objects.md)<br/>                         | Proporciona detalles sobre los requisitos especiales que se aplican a los objetos transaccionales agrupables.<br/> |
| [Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)<br/>         | Describe cómo se pueden implementar objetos agrupados para controlar cómo se reutilizan.<br/>               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de agrupación de objetos COM+](com--object-pooling-tasks.md)
</dt> </dl>

 

 




