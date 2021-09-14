---
description: Comprenda los procedimientos recomendados para los controladores de menús contextuales y varios verbos al implementar un formato de archivo personalizado en Windows Shell.
title: Procedimientos recomendados para controladores de menús contextuales y varios verbos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 14ec2e8915aa1df47ca21c6436ec963be3f590f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252074"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Procedimientos recomendados para controladores de menús contextuales y varios verbos

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Procedimientos recomendados para implementaciones de verbos](#best-practices-for-verb-implementations)
-   [Procedimientos recomendados para verbos de selección múltiple](#best-practices-for-multiple-selection-verbs)
    -   [Selecciones heterogéneos](#heterogenous-selections)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Prácticas recomendadas

Los verbos estáticos son verbos más sencillos de implementar y proporcionan una funcionalidad enriquecte. Le recomendamos encarecidamente que implemente un verbo mediante uno de los métodos de verbo estático.

### <a name="best-practices-for-verb-implementations"></a>Procedimientos recomendados para implementaciones de verbos

En la lista siguiente se representan los procedimientos recomendados para las implementaciones de verbos:

-   Elija siempre el método de verbo más sencillo que satisfaga sus necesidades.
-   Use un método de verbo estático, si es posible.
-   No realice operaciones de uso intensivo de recursos ni E/S en el subproceso de la interfaz de usuario. Tanto [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) como [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deben ser muy conservadores en el trabajo que realizan. [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) debe realizarse en otro proceso o debe crear un subproceso nuevo para evitar el bloqueo del autor de la llamada.
-   Antefiena los verbos con el nombre del proveedor de software independiente (ISV) como se muestra a continuación, `ISVName.verb` . El uso de nombres no calificados puede provocar colisiones con varios ISV que eligieron el mismo nombre de verbo.
-   Use siempre un ProgID específico de la aplicación. Dado que algunos tipos de elementos no usan esta asignación, es necesario usar nombres únicos del proveedor.
-   Coloque la interfaz de usuario en relación con el método de invocación, pero no se ejecute en un subproceso de invocador.
-   No acepte el valor devuelto **S \_ OK para** verbos canónicos pasados al método [**IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) Si lo hace, se produce un error en la implementación del verbo real que se va a invocar y devuelve un código de error para verbos canónicos. Si no admite verbos canónicos, devuelve un error cuando se encuentra un valor HIWORD(lpVerb) distinto de cero.
-   Evite el uso de **rundll32.exe** como host del verbo.
-   Al implementar [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) asegúrese de devolver el número de verbos que se han agregado al menú a través del **valor HRESULT** mediante la macro ResultFromShort.
-   Si se registra en una de las siguientes entradas de clave del Registro, tenga cuidado y asegúrese de registrar el controlador en el tipo más específico para reducir las consecuencias posiblemente no deseadas:
    -   **RAÍZ DE CLASES HKEY \_ \_\\\***
    -   **HKEY \_ CLASSES \_ ROOT \\ AllFileSystemObjects**
    -   **Carpeta RAÍZ \_ HKEY CLASSES \_ \\**
    -   **HKEY \_ CLASSES \_ ROOT \\ Directory**
-   Establezca la **tecla MayChangeDefaultMenu** solo si prevé que es posible que tenga que cambiar el verbo predeterminado en el menú contextual. Si el controlador no cambia el verbo predeterminado, no debe establecer esta clave porque, al hacerlo, el sistema carga innecesariamente el archivo DLL.
-   Minimice el trabajo que realiza [**en IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Para los controladores de menús contextuales, capture el objeto de datos pasado a **IShellExtInit::Initialize** y procese en [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)o [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Procedimientos recomendados para verbos de selección múltiple

Dado que el número de elementos de un escenario de verbo de selección múltiple puede ser grande, es importante tener en cuenta las implicaciones de rendimiento de las implementaciones de verbos. Por ejemplo, cuando un usuario busca " " en un ámbito que incluye un gran número de elementos y, a continuación, hace clic en Seleccionar todo y hace clic con el botón derecho, el verbo se presenta con una selección que puede tener miles de elementos \* en él.  Como resultado, los verbos solo deben tener en cuenta el primer elemento de la selección y el recuento total de elementos. El primer elemento se define como el elemento de la parte superior de la vista o el elemento en el que el usuario hizo clic con el botón derecho por primera vez.

En Windows 7 y versiones posteriores, el número de elementos pasados a un verbo se limita a 16 cuando se consulta un menú contextual. A continuación, el verbo se vuelve a crear y se vuelve a inicializar con la selección completa cuando se invoca ese verbo.

En algunos casos, es adecuado tener en cuenta un pequeño número de elementos fijos. Por ejemplo, es adecuado que un verbo "diff" tenga en cuenta solo los dos primeros elementos. Por lo general, no es necesario probar todos los elementos de la selección para ver si es un tipo determinado o consultar sus propiedades en cada elemento de la selección. Mire en su lugar el primer elemento y decida si es adecuado agregar el verbo.

### <a name="heterogenous-selections"></a>Selecciones heterogéneos

Los verbos optimistas se agregan automáticamente en el caso de selección múltiple, suponiendo que el verbo pueda controlar los elementos no especificados. Por el contrario, los verbos pesimistas no se agregan cuando la selección contiene elementos no especificados y solo se agregan en casos en los que el número de elementos es pequeño.

Los verbos de estilo de reproductor deben ser optimistas y omitir silenciosamente los elementos que no se controlan. Si un error al actuar en los elementos puede provocar pérdida de datos o confusión, el verbo debe advertir a los usuarios sobre los elementos que no se pueden procesar. Por ejemplo, un verbo de "copia de seguridad" debe indicar que no se pudo realizar una copia de seguridad de algunos elementos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Creación de controladores de menús contextuales](context-menu-handlers.md)
</dt> <dt>

[Personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menús contextuales](context-menu.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 



