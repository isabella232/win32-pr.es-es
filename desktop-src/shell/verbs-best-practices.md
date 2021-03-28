---
description: 'Este tema se organiza de la siguiente manera:'
title: Prácticas recomendadas para los controladores de menú contextual y varios verbos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f8b47807c4647aec274e64dbcd137833d13e23cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985767"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Prácticas recomendadas para los controladores de menú contextual y varios verbos

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Prácticas recomendadas para implementaciones de verbo](#best-practices-for-verb-implementations)
-   [Prácticas recomendadas para varios verbos de selección](#best-practices-for-multiple-selection-verbs)
    -   [Selecciones heterogéneas](#heterogenous-selections)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Prácticas recomendadas

Los verbos estáticos son verbos más sencillos para implementar y proporcionan una funcionalidad enriquecida. Le recomendamos encarecidamente que implemente un verbo con uno de los métodos estáticos Verb.

### <a name="best-practices-for-verb-implementations"></a>Prácticas recomendadas para implementaciones de verbo

La lista siguiente representa los procedimientos recomendados para las implementaciones de verbo:

-   Elija siempre el método de verbo más sencillo que se ajuste a sus necesidades.
-   Si es posible, use un método de verbo estático.
-   No realice operaciones con un uso intensivo de recursos ni e/s en el subproceso de la interfaz de usuario. Tanto [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) como [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deben ser muy conservadores en el trabajo que realizan. [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) se debe realizar en otro proceso o se debe crear un nuevo subproceso para evitar el bloqueo del llamador.
-   Prefije los verbos con el nombre del fabricante de software independiente (ISV) como se indica a continuación `ISVName.verb` . El uso de nombres no completos puede producir colisiones con varios ISV que eligen el mismo nombre de verbo.
-   Use siempre un ProgID específico de la aplicación. Dado que algunos tipos de elemento no usan esta asignación, es necesario que los nombres sean únicos para el proveedor.
-   Coloca la interfaz de usuario en relación con el método de invocación, pero no se ejecuta en un subproceso invocador.
-   No acepte el valor devuelto **S \_ OK** para verbos canónicos pasados al método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . Si lo hace, se producirá un error en la implementación del verbo real y se devolverá un código de error para verbos canónicos. Si no admite verbos canónicos, devolverá un error cuando se encuentre un valor de HIWORD distinto de cero (lpVerb).
-   Evite el uso de **rundll32.exe** como host para el verbo.
-   Al implementar [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) Asegúrese de devolver el número de verbos que se han agregado al menú a través del valor **HRESULT** mediante la macro ResultFromShort.
-   Si se registra en una de las siguientes entradas de clave del registro, preste atención y asegúrese de registrar el controlador en el tipo más específico para reducir las consecuencias posiblemente no deseadas:
    -   **HKEY \_ \_raíz \\ de clases \** _
    -   _ *HKEY \_ classes \_ root \\ AllFileSystemObjects**
    -   **\_Clase HKEY \_ raíz ( \\ carpeta raíz)**
    -   **HKEY \_ clases \_ raíz \\ Directory**
-   Establezca la clave **MayChangeDefaultMenu** solo si prevé que podría necesitar cambiar el verbo predeterminado en el menú contextual. Si el controlador no cambia el verbo predeterminado, no debe establecer esta clave, ya que esto hace que el sistema cargue el archivo DLL innecesariamente.
-   Minimice el trabajo que realiza en [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Para los controladores de menú contextual, Capture el objeto de datos pasado a **IShellExtInit:: Initialize** y, a continuación, procese en [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Prácticas recomendadas para varios verbos de selección

Dado que el número de elementos de un escenario de verbo de selección múltiple puede ser grande, es importante tener en cuenta las implicaciones de rendimiento de las implementaciones de verbo. Por ejemplo, cuando un usuario busca " \* " en un ámbito que incluye un gran número de elementos y, a continuación, hace clic en **seleccionar todo** y hace clic con el botón secundario, el verbo se presenta con una selección que puede tener miles de elementos en él. Como resultado, los verbos solo deben tener en cuenta el primer elemento de la selección y el recuento total de elementos. El primer elemento se define como el elemento en la parte superior de la vista o el elemento en el que el usuario hizo clic con el botón derecho.

En Windows 7 y versiones posteriores, el número de elementos que se pasan a un verbo está limitado a 16 cuando se consulta un menú contextual. A continuación, el verbo se vuelve a crear y se vuelve a inicializar con la selección completa cuando se invoca ese verbo.

En algunos casos, es conveniente considerar un pequeño número de elementos fijos. Por ejemplo, es adecuado para un verbo "diff" considerar solo los dos primeros elementos. Por lo general, no es necesario probar todos los elementos de la selección para ver si se trata de un tipo determinado, o bien realizar una consulta en todos los elementos de la selección para sus propiedades. Fíjese en el primer elemento y decida si es adecuado agregar el verbo.

### <a name="heterogenous-selections"></a>Selecciones heterogéneas

Los verbos optimistas se agregan automáticamente en el caso de selección múltiple, suponiendo que los elementos no inspeccionados se pueden controlar mediante el verbo. En cambio, los verbos pesimistas no se agregan cuando la selección contiene elementos sin inspeccionar y solo se agregan en casos en los que el número de elementos es pequeño.

Los verbos de estilo de reproductor deben ser optimistas y omitir silenciosamente los elementos que no se controlan. Si un error al actuar en los elementos puede provocar la pérdida de datos o confusión, el verbo debe advertir a los usuarios sobre los elementos que no se pueden procesar. Por ejemplo, un verbo "backup" debería indicar que no se pudo realizar una copia de seguridad de algunos elementos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Crear controladores de menú contextual](context-menu-handlers.md)
</dt> <dt>

[Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menú contextual](context-menu.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 



