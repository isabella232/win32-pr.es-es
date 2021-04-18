---
description: Información general sobre el modelo en cascada para la clase RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: El modelo RealTimeStylus en cascada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564225"
---
# <a name="the-cascaded-realtimestylus-model"></a>El modelo RealTimeStylus en cascada

El modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada permite usar dos objetos **RealTimeStylus** , cada uno de los cuales se ejecuta en un subproceso diferente. Con este modelo, se adjunta un objeto **RealTimeStylus** secundario a un objeto **RealTimeStylus** primario. El objeto **RealTimeStylus** secundario se adjunta como el único complemento asincrónico en la colección de complementos asincrónica del objeto **RealTimeStylus** principal.

El modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada puede ser útil en los escenarios siguientes.

-   Puede Agregar a la colección de complementos sincrónicos del objeto [**RealTimeStylus**](realtimestylus-class.md) el acceso en tiempo real al flujo de datos del lápiz de Tablet PC, como el reconocimiento de gestos de varios trazos.
-   Puede distribuir la carga de cálculo de los complementos sincrónicos en dos subprocesos, lo que reduce los retrasos en la recopilación de entradas manuscritas en algunos Tablet PC.

En el diagrama siguiente se ilustra el flujo de datos del lápiz de Tablet PC a través de dos objetos [**RealTimeStylus**](realtimestylus-class.md) en cascada y sus colecciones de complementos.

![Ilustración que muestra el flujo de datos RealTimeStylus en cascada](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

En este diagrama, la letra "A" del círculo representa los datos del lápiz de Tablet PC que ya han sido procesados por los objetos [**RealTimeStylus**](realtimestylus-class.md) principal y secundario, y se han colocado en la cola de salida del objeto **RealTimeStylus** secundario. La letra "B" en el círculo representa los datos del lápiz de Tablet PC que ya ha procesado el objeto **RealTimeStylus** principal y se han agregado a la cola de salida del objeto **RealTimeStylus** principal y aún no se ha enviado al objeto **RealTimeStylus** secundario. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** principal. Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

## <a name="constraints"></a>Restricciones

Si usa el constructor [**RealTimeStylus**](realtimestylus-class.md) predeterminado, se crea un objeto **RealTimeStylus** que solo puede aceptar la entrada de otro objeto **RealTimeStylus** .

En la lista siguiente se describen las restricciones asociadas al uso del modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada.

-   Solo se pueden usar dos objetos [**RealTimeStylus**](realtimestylus-class.md) , un objeto **RealTimeStylus** primario y un objeto **RealTimeStylus** secundario.
-   El objeto [**RealTimeStylus**](realtimestylus-class.md) principal se debe crear con un constructor que use el parámetro **attachedControl** o *Handle* . El objeto **RealTimeStylus** secundario debe crearse con el constructor sin argumentos.
-   El objeto [**RealTimeStylus**](realtimestylus-class.md) secundario debe ser el único complemento asincrónico de la colección de complementos asincrónica del objeto **RealTimeStylus** principal.
-   Un objeto [**RealTimeStylus**](realtimestylus-class.md) secundario solo se puede asociar a un objeto **RealTimeStylus** primario a la vez. Si se agrega a un segundo objeto **RealTimeStylus** primario, el método [Add](/previous-versions/ms824814(v=msdn.10)) produce una excepción y el objeto **RealTimeStylus** secundario no se adjunta al segundo objeto **RealTimeStylus** primario.
-   Se modifica el comportamiento de algunos de los miembros del objeto [**RealTimeStylus**](realtimestylus-class.md) secundarios. En la tabla siguiente se describe el comportamiento modificado de estos miembros.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Miembro</th>
    <th>Comportamiento</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></td>
    <td>Este método devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, este método devuelve el valor predeterminado.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></td>
    <td>Este método genera una excepción <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .<br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></td>
    <td>Este método devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, este método devuelve una matriz vacía.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></td>
    <td>Al obtener esta propiedad, se devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, al obtener esta propiedad se devuelve el valor predeterminado.<br/>
    <blockquote>
    [!Note]<br />
Al establecer esta propiedad, se produce una excepción <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></td>
    <td>Al obtener esta propiedad, se devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, al obtener esta propiedad se devuelve el valor predeterminado.<br/>
    <blockquote>
    [!Note]<br />
Al establecer esta propiedad, se produce una excepción <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   Se espera que el objeto primario [**RealTimeStylus**](realtimestylus-class.md) deje de funcionar cuando se desecha el **RealTimeStylus** secundario.

 

 
