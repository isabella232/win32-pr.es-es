---
description: Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714855"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS

COM+ quita o reduce varias limitaciones de la depuración con Microsoft Visual Basic 6,0 y MTS. En la lista siguiente se resumen los cambios que puede esperar con COM+:

-   Depurar varios componentes: en COM+, puede depurar escenarios en los que un cliente que se ejecuta en una instancia del IDE realiza llamadas a cualquier número de archivos DLL que se ejecutan en otro como grupo de proyectos. Los objetos de los proyectos DLL agrupados pueden llamarse entre sí de forma arbitraria, y fluyen el contexto según sea necesario. Por supuesto, esto también funciona cuando los archivos dll y el cliente están en el mismo grupo de proyectos en la misma instancia del IDE.

-   Limitaciones de depuración en eventos de clase \_ Initialize y de \_ finalización de clase: con com+, puede colocar el código en la clase \_ Initialize y \_ finalizar los eventos de un componente de aplicación com+ incluso si ese código intenta tener acceso al objeto o su objeto de contexto correspondiente. Puede establecer puntos de interrupción allí y usar inspecciones. También puede establecer puntos de interrupción en el evento de la clase \_ Terminate.

    Aunque ya no se necesita como solución alternativa, puede implementar la interfaz [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) y usar los métodos de [**activación**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) y [**desactivación**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) si necesita ejecutar código durante el inicio y el apagado del componente. Ahora también puede colocar puntos de interrupción en el código para los métodos **Deactivate** o [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) .

-   Ver objetos MTS: con COM+, puede Agregar inspecciones para las variables de objeto devueltas por COM+, incluidos los valores devueltos de los métodos [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef), [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)y [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) .

-   Mayor estabilidad cuando se produce un error en los componentes: en COM+, un error de componente ya no se detiene siempre Visual Basic (que se ejecuta en el mismo proceso que el componente depurado). Por ejemplo, ahora la compatibilidad con errores de reactivación Just-in-Time (JIT) permite examinar el contexto del objeto durante la depuración.

-   El depurador puede reactivar los objetos publicados por COM+, como con MTS, Visual Basic 6,0 puede reactivar los objetos COM+ mientras se depura en un solo paso a través de un cliente. Debido al modo en que Visual Basic 6,0 detecta información acerca de los objetos, este comportamiento es el esperado. Por ejemplo, considere el siguiente código:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Si el obj. El método de prueba llama a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), com+ libera de forma inmediata a obj de la memoria, pero obj no se ha establecido todavía en nada. Cuando es obj. Test devuelve, el depurador de Visual Basic llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en obj para la interfaz [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) . El contenedor de contexto asociado a obj crea una nueva instancia de MyApp. MyClass para atender la llamada **QueryInterface** . Como resultado, verá este objeto no inicializado en el depurador después de obj. La prueba se ha devuelto. Este objeto solo aparece en el depurador y se quita mediante la siguiente instrucción para establecer obj en Nothing.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Depuración en el IDE de Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
