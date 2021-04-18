---
description: Al configurar un componente que se va a agrupar, COM+ mantendrá las instancias del mismo en un grupo, listo para activarse para cualquier cliente que solicite el componente. Cualquier solicitud de creación de objetos se controlará a través del administrador de grupos.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Cómo funciona la agrupación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714833"
---
# <a name="how-object-pooling-works"></a>Cómo funciona la agrupación de objetos

Al configurar un componente que se va a agrupar, COM+ mantendrá las instancias del mismo en un grupo, listo para activarse para cualquier cliente que solicite el componente. Cualquier solicitud de creación de objetos se controlará a través del administrador de grupos.

Los grupos se configuran y mantienen en cada componente. Un grupo consta de objetos homogéneos que comparten el mismo CLSID. La única excepción son los objetos transaccionales, para los que se mantienen los subgrupos que contienen objetos que tienen afinidad de transacción mientras hay una transacción pendiente.

Cuando se inicia la aplicación, el grupo se rellenará hasta el nivel mínimo que haya especificado administrativamente, siempre y cuando la creación del objeto se realice correctamente. A medida que las solicitudes de cliente para el componente se encuentran en, se satisfacen en una base de la primera vez que se atiende desde el grupo. Si no hay ningún objeto agrupado disponible y el grupo aún no tiene el nivel máximo especificado, se creará y activará un nuevo objeto para el cliente.

Cuando el grupo alcanza su nivel máximo, las solicitudes de cliente se ponen en cola y recibirán el primer objeto disponible del grupo. El número de objetos, incluidos los activados y desactivados, nunca superará el valor máximo del grupo. Las solicitudes de creación de objetos agotarán el tiempo de espera después de un período especificado administrativamente para que pueda controlar cuánto tiempo esperarán los clientes para la creación de objetos. Tras un error de tiempo de espera, el cliente obtendrá el error E \_ tiempo de espera de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Siempre que sea posible, COM+ intentará volver a usar un objeto después de que un cliente lo libere, hasta que el grupo alcance su nivel máximo. El objeto es responsable de supervisar su estado para determinar si se puede reutilizar y devolver un valor adecuado para [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Cuando se crea un objeto agrupado, se agrega a un objeto más grande que administrará la duración del objeto. El objeto externo llama a los métodos en [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) en los momentos adecuados del ciclo de vida del objeto, como se indica a continuación:

-   Se llama al método [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) cuando el objeto se devuelve a un cliente, que se activa en un contexto específico.
-   Se llama al método de [**desactivación**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) cada vez que el cliente libera un objeto o, en el caso de un objeto activado en JIT, cuando se desactiva.
-   Se llama al método [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) cada vez que un objeto se va a devolver al grupo general. Si el objeto detecta que algún recurso reutilizable está en mal estado, debería devolver **false** para este método y el administrador del grupo descartará el objeto.

Un objeto no necesita necesariamente implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Si no es así, las instancias siempre se volverán a usar hasta que se alcance el nivel máximo del grupo.

Para obtener más información sobre cómo configurar los componentes que se van a agrupar, vea [configurar un componente para agrupar](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Mejorar el rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Agrupar objetos transaccionales](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
