---
title: Acciones de tarea
description: Los elementos de trabajo que realiza una tarea se denominan acciones. Una tarea puede tener una sola acción o un máximo de 32 acciones. Tenga en cuenta que cuando se especifican varias acciones, se ejecutan secuencialmente.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- acciones Programador de tareas
- acciones Programador de tareas, descritas
- acciones Programador de tareas, ejecutar acción
- acciones Programador de tareas, acción del controlador COM
- ejecutar Programador de tareas de acción
- Programador de tareas de acción del controlador COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103787599"
---
# <a name="task-actions"></a>Acciones de tarea

Los elementos de trabajo que realiza una tarea se denominan acciones. Una tarea puede tener una sola acción o un máximo de 32 acciones. Tenga en cuenta que cuando se especifican varias acciones, se ejecutan secuencialmente.

## <a name="types-of-actions"></a>Tipos de acciones

La siguiente tabla de acciones describe el tipo de trabajo o acciones que puede realizar una tarea.

| Tipo de acción      | Descripción                                                             |
|---------------------|-------------------------------------------------------------------------|
| Acción de comcontrolador   | Esta acción activa un controlador COM.                                        |
| Acción exec         | Esta acción ejecuta una operación de línea de comandos, como iniciar el Bloc de notas. |
| Acción de correo electrónico       | Esta acción envía un correo electrónico cuando se desencadena una tarea.                    |
| Mostrar acción de mensaje | Esta acción muestra un cuadro de mensaje con un mensaje y título especificados.     |



 

## <a name="specifying-actions"></a>Especificar acciones

Las acciones de una tarea se especifican cuando la tarea se define y se almacena en una colección de acciones utilizada por el servicio de Programador de tareas. En la tabla siguiente se incluyen vínculos a temas de referencia para las API y los elementos XML que están asociados a acciones.

Para obtener más información y ejemplos sobre cómo usar las interfaces de Programador de tareas, los objetos de scripting y XML, vea [usar el programador de tareas](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>API de interfaz para el desarrollo en C++



| API                                                                    | Descripción                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Propiedad Actions de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Obtiene o establece las acciones realizadas por la tarea.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Contiene las acciones realizadas por la tarea.                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Representa una acción que activa un controlador.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Representa una acción que ejecuta una operación de la línea de comandos. |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Representa una acción que envía un mensaje de correo electrónico.            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Representa una acción que muestra un cuadro de mensaje.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>Scripting de API de objetos para el desarrollo de scripting



| API                                                      | Descripción                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition. Actions**](taskdefinition-actions.md) | Obtiene o establece las acciones realizadas por la tarea.              |
| [**ActionCollection**](actioncollection.md)             | Contiene las acciones realizadas por la tarea.                  |
| [**ComHandlerAction**](comhandleraction.md)             | Representa una acción que activa un controlador.                   |
| [**ExecAction**](execaction.md)                         | Representa una acción que ejecuta una operación de la línea de comandos. |
| [**EmailAction**](emailaction.md)                       | Representa una acción que envía un mensaje de correo electrónico.            |
| [**ShowMessageAction**](showmessageaction.md)           | Representa una acción que muestra un cuadro de mensaje.               |



 

### <a name="xml-elements"></a>Elementos XML



| Elemento                                                                    | Descripción                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md)            | Define las acciones realizadas por la tarea.                   |
| [**Controlador**](taskschedulerschema-comhandler-actiongroup-element.md)   | Representa una acción que activa un controlador.                   |
| [**Ejec**](taskschedulerschema-exec-actiongroup-element.md)               | Representa una acción que ejecuta una operación de la línea de comandos. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Representa una acción que envía un mensaje de correo electrónico.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Representa una acción que muestra un cuadro de mensaje.               |



 

## <a name="using-variables-in-action-properties"></a>Usar variables en las propiedades de acción

Algunas propiedades de acción que son de tipo **BSTR** pueden contener variables $ (Arg0), $ (arg1),..., $ (Arg32) en sus valores de cadena. Estas variables se reemplazan por los valores que se especifican en el parámetro *params* de los métodos [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) y [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) o se encuentran dentro del desencadenador de eventos para la tarea. En la tabla siguiente se enumeran las propiedades de acción que pueden usar variables en sus valores de cadena.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Acción</th>
<th>Propiedades</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Acción del controlador COM</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propiedad ClassId de IComHandlerAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propiedad de datos de IComHandlerAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="comhandleraction-classid.md"><strong>ComHandlerAction. ClassId</strong></a></li>
<li><a href="comhandleraction-data.md"><strong>ComHandlerAction. Data</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Acción de correo electrónico</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propiedad Body de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propiedad Server de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propiedad Subject de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Propiedad to de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propiedad CC de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propiedad BCC de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propiedad ReplyTo de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Propiedad From de IEmailAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="emailaction-body.md"><strong>EmailAction. Body</strong></a></li>
<li><a href="emailaction-server.md"><strong>EmailAction. Server</strong></a></li>
<li><a href="emailaction-subject.md"><strong>EmailAction. Subject</strong></a></li>
<li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li>
<li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li>
<li><a href="emailaction-bcc.md"><strong>EmailAction. BCC</strong></a></li>
<li><a href="emailaction-replyto.md"><strong>EmailAction. ReplyTo</strong></a></li>
<li><a href="emailaction-from.md"><strong>EmailAction. from</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Acción exec</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propiedad arguments de IExecAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propiedad WorkingDirectory de IExecAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="execaction-arguments.md"><strong>ExecAction. arguments</strong></a></li>
<li><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Mostrar acción de mensaje</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propiedad title de IShowMessageAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propiedad MessageBody de IShowMessageAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="showmessageaction-title.md"><strong>ShowMessageAction. title</strong></a></li>
<li><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
</dt> </dl>

 

 





