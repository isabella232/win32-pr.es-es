---
description: Información general del modelo en cascada para la clase RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: El modelo RealTimeStylus en cascada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf848f1382a8c6a54f58fb6db864ece165c7cff2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468002"
---
# <a name="the-cascaded-realtimestylus-model"></a>El modelo RealTimeStylus en cascada

El modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada permite usar dos objetos **RealTimeStylus,** cada uno de los que se ejecuta en un subproceso diferente. Con este modelo, se adjunta un objeto **RealTimeStylus** secundario a un objeto **RealTimeStylus** principal. El objeto **RealTimeStylus** secundario se adjunta como el único complemento asincrónico en la colección de complementos asincrónicos del objeto **RealTimeStylus** principal.

El modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada puede ser útil en los escenarios siguientes.

-   Puede agregar ciertas tareas que pueden ser exigentes desde el punto de vista computacional pero que aún requieren acceso en tiempo real al flujo de datos del lápiz de tableta, como el reconocimiento de gestos multistroke, a la colección de complementos sincrónicos del objeto [**RealTimeStylus**](realtimestylus-class.md) secundario.
-   Puede repartir la carga computacional de los complementos sincrónicos en dos subprocesos, lo que reduce los retrasos en la recopilación de entrada de lápiz en algunos equipos de tableta.

En el diagrama siguiente se muestra el flujo de datos de lápiz de tableta a través de dos objetos [**RealTimeStylus**](realtimestylus-class.md) en cascada y sus colecciones de complementos.

![ilustración que muestra el flujo de datos en cascada en tiempo real](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

En este diagrama, el círculo con la letra "A" representa los datos del lápiz de tableta que ya han sido procesados por los objetos [**RealTimeStylus**](realtimestylus-class.md) principal y secundario y que se han colocado en la cola de salida del objeto **RealTimeStylus secundario.** El círculo con la letra "B" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** principal ya ha procesado y agregado a la cola de salida del objeto **RealTimeStylus** principal y aún no se ha enviado al objeto **RealTimeStylus secundario.** El círculo con letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** principal está procesando actualmente. Se envía a la colección de complementos sincrónica y se coloca en la cola de salida. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

## <a name="constraints"></a>Restricciones

Si usa el constructor [**RealTimeStylus**](realtimestylus-class.md) predeterminado, cree un objeto **RealTimeStylus** que solo pueda aceptar la entrada de otro **objeto RealTimeStylus.**

En la lista siguiente se describen las restricciones asociadas al uso del modelo [**RealTimeStylus en**](realtimestylus-class.md) cascada.

-   Solo se pueden usar dos objetos [**RealTimeStylus,**](realtimestylus-class.md) un objeto **RealTimeStylus** principal y un objeto **RealTimeStylus** secundario.
-   El objeto [**RealTimeStylus**](realtimestylus-class.md) principal debe crearse con un constructor que use el **parámetro attachedControl** o *handle.* El objeto **Secundario RealTimeStylus** debe crearse con el constructor sin argumento.
-   El objeto [**Secundario RealTimeStylus**](realtimestylus-class.md) debe ser el único complemento asincrónico de la colección de complementos asincrónicos del objeto **RealTimeStylus** principal.
-   Un objeto [**RealTimeStylus**](realtimestylus-class.md) secundario solo se puede adjuntar a un objeto **RealTimeStylus** principal a la vez. Si se agrega a un segundo objeto **RealTimeStylus** principal, el método [Add](/previous-versions/ms824814(v=msdn.10)) produce una excepción y el objeto **RealTimeStylus** secundario no está asociado al segundo objeto **RealTimeStylus principal.**
-   Se modifica el comportamiento de algunos de los miembros del objeto [**RealTimeStylus**](realtimestylus-class.md) secundario. En la tabla siguiente se describe el comportamiento modificado de estos miembros.

    

    
| Miembro | Comportamiento | 
|--------|----------|
| <a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a> | Este método devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.<br /> Si el <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> principal, este método devuelve el valor predeterminado.<br /> | 
| <a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a> | Este método genera una <a href="/dotnet/api/system.invalidoperationexception">excepción InvalidOperationException.</a><br /> | 
| <a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a> | Este método devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.<br /> Si el <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> principal, este método devuelve una matriz vacía.<br /> | 
| <a href="/previous-versions/ms824832(v=msdn.10)">Habilitado</a> | Al obtener esta propiedad, se devuelve la información del <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> principal.<br /> Si el <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> principal, al obtener esta propiedad se devuelve el valor predeterminado.<br /><blockquote>    [!Note]<br />    Establecer esta propiedad genera una <a href="/dotnet/api/system.invalidoperationexception">excepción InvalidOperationException.</a>    </blockquote><br /> | 
| <a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a> | Al obtener esta propiedad, se devuelve la información del <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> principal.<br /> Si el <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> principal, al obtener esta propiedad se devuelve el valor predeterminado.<br /><blockquote>    [!Note]<br />    Establecer esta propiedad genera una <a href="/dotnet/api/system.invalidoperationexception">excepción InvalidOperationException.</a>    </blockquote><br /> | 


    

     

-   Se espera que el objeto [**RealTimeStylus**](realtimestylus-class.md) primario deje de funcionar cuando se **desechar el elemento secundario RealTimeStylus.**

 

 
