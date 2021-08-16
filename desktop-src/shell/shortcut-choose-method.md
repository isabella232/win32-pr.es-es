---
description: Elija un método de menú contextual estático o dinámico al implementar un formato de archivo personalizado en Windows Shell.
title: Elegir un método de menú contextual estático o dinámico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c910407dbd9de9f12853973f9891fe092a0603ca50a03e59183697b0f92b07e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968324"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Elegir un método de menú contextual estático o dinámico

Este tema se organiza de la siguiente manera:

-   [Elegir un método verbo](#choose-a-verb-method)
    -   [Métodos de verbo estáticos](#static-verb-methods)
    -   [Métodos de verbo dinámico preferidos](#preferred-dynamic-verb-methods)
    -   [Métodos de verbo dinámicos desaconsejados](#discouraged-dynamic-verb-methods)
-   [Extender un menú contextual](#extend-a-shortcut-menu)
-   [Compatibilidad con métodos verbo por sistema operativo](#support-for-verb-methods-by-operating-system)
-   [Temas relacionados](#related-topics)

## <a name="choose-a-verb-method"></a>Elegir un método verbo

Se recomienda encarecidamente que implemente un menú contextual mediante uno de los métodos de verbo estáticos.

### <a name="static-verb-methods"></a>Métodos de verbo estáticos

Los verbos estáticos son los verbos más sencillos de implementar, pero todavía proporcionan una funcionalidad enriquecte. Elija siempre el método de menú contextual más sencillo que satisfaga sus necesidades.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verbo estático</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess con</strong></a> parámetros de línea de comandos</td>
<td>Este es el medio más sencillo y familiar de implementar un verbo estático. Un proceso se invoca mediante una llamada a la <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>función CreateProcess</strong></a> con los archivos seleccionados y los parámetros opcionales pasados como línea de comandos. Se abrirá el archivo o la carpeta.<br/> Este método tiene las siguientes limitaciones:
<ul>
<li>La longitud de la línea de comandos está limitada a 2000 caracteres, lo que limita el número de elementos que el verbo puede controlar.</li>
<li>Solo se puede usar con elementos del sistema de archivos.</li>
<li>No habilita el nuevo uso de un proceso que ya se está ejecutando.</li>
<li>Requiere que se instale un ejecutable para controlar el verbo.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Una activación verbo basada en COM significa que admite la activación en proceso o fuera de proceso. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget también</strong></a> admite el nuevo uso de un controlador que ya se está ejecutando cuando un servidor local implementa la interfaz <strong>IDropTarget.</strong> También expresa perfectamente los elementos a través del objeto de datos serializados y proporciona una referencia a la cadena de sitio que invoca para que pueda interactuar con el invocador a través de <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</td>
</tr>
<tr class="odd">
<td>Windows 7 y versiones posteriores: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>El método de implementación más directo. Dado que se trata de un método de invocación basado en COM (como DropTarget), esta interfaz admite la activación en proceso y fuera de proceso. El verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>e IObjectWithSelection y,</strong></a>opcionalmente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Los elementos se pasan directamente como una matriz de elementos de Shell y hay más parámetros del invocador disponibles para la implementación del verbo, incluido el punto de invocación, el estado del teclado, etc.</td>
</tr>
<tr class="even">
<td>Windows 7 y versiones posteriores:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Permite que los orígenes de datos que proporcionan sus comandos de módulo de comandos a través <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>de IExplorerCommandProvider</strong></a> usen esos comandos como verbos en un menú contextual. Dado que esta interfaz solo admite la activación en proceso, se recomienda su uso por parte de orígenes de datos de Shell que necesitan compartir la implementación entre comandos y menús contextuales.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand es**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) un híbrido entre un verbo estático y dinámico. **IExplorerCommand** se declaró en Windows Vista, pero su capacidad para implementar un verbo en un menú contextual es nueva Windows 7.

 

Para obtener más información sobre [**las consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y Shell para los atributos de asociación de archivos, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Métodos de verbo dinámico preferidos

Se prefieren los siguientes métodos de verbo dinámico:



| Tipo de verbo                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo estático (enumerado en la tabla anterior) + Sintaxis de consulta avanzada (AQS)                  | Esta opción obtiene visibilidad dinámica del verbo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 y versiones posteriores: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Esta opción permite una implementación común de verbos y comandos de explorador que se muestran en el módulo de comandos Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 y versiones posteriores: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo estático | Esta opción también obtiene visibilidad dinámica de verbos. Se trata de un modelo híbrido en el que se usa un controlador en proceso simple para calcular si un verbo estático determinado debe estar indispuesto. Esto se puede aplicar a todos los métodos de implementación de verbo estáticos para lograr un comportamiento dinámico y minimizar la exposición de la lógica en proceso. [**IExplorerCommandState tiene**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) la ventaja de ejecutarse en un subproceso en segundo plano y, por tanto, evita que la interfaz de usuario se queje. Es considerablemente más sencillo que [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) |



 

### <a name="discouraged-dynamic-verb-methods"></a>Métodos de verbo dinámicos desaconsejados

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es el método más eficaz, pero también el más complicado de implementar. Se basa en objetos COM en proceso que se ejecutan en el subproceso del autor de la llamada, que normalmente Windows Explorer, pero puede ser cualquier aplicación que hospeda los elementos. **IContextMenu admite** visibilidad de verbos, ordenación y dibujo personalizado. Algunas de estas características se han agregado a las características del verbo estático, como un icono que se va a asociar a un comando e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) para tratar con la visibilidad.

Si debe extender el menú contextual de un tipo de archivo mediante el registro de un verbo dinámico para el tipo de archivo, siga las instrucciones proporcionadas en Personalización de un menú contextual mediante [verbos dinámicos](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Extender un menú contextual

Después de elegir un método verbo, puede extender un menú contextual para un tipo de archivo registrando un verbo estático para el tipo de archivo. Para obtener más información, vea [Crear controladores de menú contextual](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Compatibilidad con métodos verbo por sistema operativo

La compatibilidad con los métodos de invocación de verbos por sistema operativo se muestra en la tabla siguiente.



| Verb (método)          | Windows XP | Windows Vista | Windows 7 y posteriores |
|----------------------|------------|---------------|----------------------|
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple](verbs-best-practices.md)
</dt> <dt>

[Creación de controladores de menús contextuales](context-menu-handlers.md)
</dt> <dt>

[Personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menús contextuales](context-menu.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> </dl>

 

 
