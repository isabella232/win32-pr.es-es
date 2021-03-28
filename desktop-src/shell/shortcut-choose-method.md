---
description: 'Este tema se organiza de la siguiente manera:'
title: Elegir un método de menú contextual estático o dinámico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082959"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Elegir un método de menú contextual estático o dinámico

Este tema se organiza de la siguiente manera:

-   [Elegir un método de verbo](#choose-a-verb-method)
    -   [Métodos de verbo estáticos](#static-verb-methods)
    -   [Métodos de verbo dinámico preferidos](#preferred-dynamic-verb-methods)
    -   [Métodos de verbo dinámico desaconsejados](#discouraged-dynamic-verb-methods)
-   [Extender un menú contextual](#extend-a-shortcut-menu)
-   [Compatibilidad con métodos de verbo por sistema operativo](#support-for-verb-methods-by-operating-system)
-   [Temas relacionados](#related-topics)

## <a name="choose-a-verb-method"></a>Elegir un método de verbo

Se recomienda encarecidamente implementar un menú contextual con uno de los métodos estáticos Verb.

### <a name="static-verb-methods"></a>Métodos de verbo estáticos

Los verbos estáticos son los verbos más sencillos para implementar, pero aún proporcionan una funcionalidad enriquecida. Elija siempre el método de menú contextual más sencillo que satisfaga sus necesidades.



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
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> con parámetros de la línea de comandos</td>
<td>Este es el medio más sencillo y familiar para implementar un verbo estático. Un proceso se invoca a través de una llamada a la función <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> con los archivos seleccionados y los parámetros opcionales pasados como línea de comandos. Se abrirá el archivo o la carpeta.<br/> Este método tiene las siguientes limitaciones:
<ul>
<li>La longitud de la línea de comandos está limitada a 2000 caracteres, lo que limita el número de elementos que puede controlar el verbo.</li>
<li>Solo se puede usar con elementos del sistema de archivos.</li>
<li>No permite volver a utilizar un proceso que ya se está ejecutando.</li>
<li>Requiere que se instale un ejecutable para controlar el verbo.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Una activación de verbo basada en COM significa que admite la activación en proceso o fuera de proceso. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> también admite la reutilización de un controlador que ya se está ejecutando cuando un servidor local implementa la interfaz <strong>IDropTarget</strong> . También expresa perfectamente los elementos a través del objeto de datos de serialización y proporciona una referencia a la cadena de sitios de invocación para que pueda interactuar con el invocador a través de <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</td>
</tr>
<tr class="odd">
<td>Windows 7 y versiones posteriores: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>Método de implementación más directo. Dado que se trata de un método de invocación basado en COM (como DropTarget), esta interfaz admite la activación en proceso y fuera de proceso. El verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>y, opcionalmente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Los elementos se pasan directamente como una matriz de elementos de Shell y más de los parámetros del Invocador están disponibles para la implementación del verbo, incluido el punto de invocación, el estado del teclado, etc.</td>
</tr>
<tr class="even">
<td>Windows 7 y versiones posteriores:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Habilita los orígenes de datos que proporcionan los comandos del módulo de comandos a través de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> para usar esos comandos como verbos en un menú contextual. Dado que esta interfaz solo admite la activación en proceso, se recomienda para su uso por parte de los orígenes de datos de Shell que necesitan compartir la implementación entre los comandos y los menús contextuales.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) es un híbrido entre un verbo estático y dinámico. **IExplorerCommand** se declaró en Windows Vista, pero su capacidad para implementar un verbo en un menú contextual es nueva en Windows 7.

 

Para obtener más información sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y las consultas de Shell para los atributos de Asociación de archivos, consulte [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Métodos de verbo dinámico preferidos

Se prefieren los siguientes métodos de verbo dinámico:



| Tipo de verbo                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo estático (enumerado en la tabla anterior) + sintaxis de consulta avanzada (AQS)                  | Esta opción obtiene la visibilidad del verbo dinámico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 y versiones posteriores: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Esta opción habilita una implementación común de verbos y comandos del explorador que se muestran en el módulo de comandos en el explorador de Windows.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 y versiones posteriores: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo estático | Esta opción también obtiene visibilidad del verbo dinámico. Es un modelo híbrido en el que se usa un sencillo controlador en proceso para calcular si un verbo estático determinado debe ser aparecerá. Esto puede aplicarse a todos los métodos de implementación de verbos estáticos para lograr un comportamiento dinámico y minimizar la exposición de la lógica en proceso. [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) tiene la ventaja de que se ejecuta en un subproceso en segundo plano y, por tanto, evita los bloqueos de la interfaz de usuario. Es mucho más sencillo que [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). |



 

### <a name="discouraged-dynamic-verb-methods"></a>Métodos de verbo dinámico desaconsejados

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es el método más eficaz, pero también el más complicado de implementar. Se basa en objetos COM en proceso que se ejecutan en el subproceso del autor de la llamada, que normalmente es el explorador de Windows, pero puede ser cualquier aplicación que hospede los elementos. **IContextMenu** admite la visibilidad de verbos, el orden y el dibujo personalizado. Algunas de estas características se han agregado a las características de verbo estático, como un icono que se va a asociar a un comando, y [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) para tratar la visibilidad.

Si debe extender el menú contextual de un tipo de archivo registrando un verbo dinámico para el tipo de archivo, siga las instrucciones que se proporcionan en [Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Extender un menú contextual

Después de elegir un método de verbo, puede extender un menú contextual para un tipo de archivo registrando un verbo estático para el tipo de archivo. Para obtener más información, vea [crear controladores de menús contextuales](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Compatibilidad con métodos de verbo por sistema operativo

En la tabla siguiente se enumeran los métodos de invocación de verbos por sistema operativo.



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | Windows XP | Windows Vista | Windows 7 y versiones posteriores |
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección](verbs-best-practices.md)
</dt> <dt>

[Crear controladores de menú contextual](context-menu-handlers.md)
</dt> <dt>

[Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menús contextuales y controladores de menú contextual](context-menu.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> </dl>

 

 
