---
description: Al configurar un componente que se va a agrupar, COM+ mantendrá las instancias de él en un grupo, listas para activarse para cualquier cliente que solicite el componente. Las solicitudes de creación de objetos se controlarán a través del administrador de grupo.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Funcionamiento de la agrupación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df937dd8e3d7a2fb111c7825df101cd2b53f6f39a94326efb1eafe878d74daa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954045"
---
# <a name="how-object-pooling-works"></a>Funcionamiento de la agrupación de objetos

Al configurar un componente que se va a agrupar, COM+ mantendrá las instancias de él en un grupo, listas para activarse para cualquier cliente que solicite el componente. Las solicitudes de creación de objetos se controlarán a través del administrador de grupo.

Los grupos se configuran y mantienen por componente. Un grupo consta de objetos homogéneos que comparten el mismo CLSID. La única excepción es para los objetos transaccionales, para los que se mantienen subpools que contienen objetos que tienen afinidad de transacción mientras una transacción está pendiente.

Cuando se inicia la aplicación, el grupo se rellenará hasta el nivel mínimo que haya especificado administrativamente, siempre que la creación del objeto se complete correctamente. A medida que llegan las solicitudes de cliente para el componente, se satisfacen por primera vez desde el grupo. Si no hay ningún objeto agrupado disponible y el grupo aún no está en el nivel máximo especificado, se crea y se activa un nuevo objeto para el cliente.

Cuando el grupo alcanza su nivel máximo, las solicitudes de cliente se ponen en cola y recibirán el primer objeto disponible del grupo. El número de objetos, incluidos activados y desactivados, nunca superará el valor máximo del grupo. Las solicitudes de creación de objetos pasarán el tiempo de espera después de un período especificado administrativamente para que pueda controlar cuánto tiempo esperarán los clientes a la creación del objeto. Tras un error de tiempo de espera, el cliente recuperará el error E \_ TIMEOUT de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Siempre que sea posible, COM+ intentará reutilizar un objeto después de que un cliente lo libere, hasta que el grupo alcance su nivel máximo. El objeto es responsable de supervisar su estado para determinar si se puede reutilizar y debe devolver un valor adecuado para [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Cuando se crea un objeto agrupado, se agrega a un objeto mayor que administrará la duración del objeto. El objeto externo llama a métodos [**en IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) en los momentos adecuados del ciclo de vida del objeto, como se muestra a continuación:

-   Se [**llama al**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) método Activate cada vez que el objeto se devuelve a un cliente, activado en un contexto específico.
-   Se llama al método [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) cada vez que el cliente libera un objeto o, en el caso de un objeto activado JIT, cuando se desactiva.
-   Se [**llama al método CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) cada vez que se va a devolver un objeto al grupo general. Si el objeto detecta que algún recurso reutilizable está en mal estado, debe devolver **FALSE** para este método y el administrador del grupo descartará el objeto.

Un objeto no necesita necesariamente implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Si no es así, las instancias siempre se volverán a usar hasta que se alcance el nivel máximo del grupo.

Para obtener más información sobre cómo configurar los componentes que se agruparán, vea [Configuring a Component to Be Pooled](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas de constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Mejora del rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Agrupación de objetos transaccionales](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
