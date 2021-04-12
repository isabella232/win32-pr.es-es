---
title: Métodos IPaperSink
description: El copaper expone la interfaz IConnectionPointContainer para que los clientes puedan conectarse al copaper con el fin de recibir notificaciones de los eventos especificados que se producen en el copaper.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8dee615b278c5214ad1efa3c10d22759620103
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271326"
---
# <a name="ipapersink-methods"></a>Métodos IPaperSink

El copaper expone la interfaz [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) para que los clientes puedan conectarse al copaper con el fin de recibir notificaciones de los eventos especificados que se producen en el copaper. Al exponer esta interfaz, el copapel se convierte en un objeto conectable. Un cliente puede llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para esta interfaz y utilizarla para obtener los puntos de conexión del objeto. La participación del cliente en este esquema se trata en el ejemplo de **StoClien** asociado.

Básicamente, el cliente implementa lo que se denomina receptor en forma de un objeto receptor con una interfaz receptora. La interfaz de receptor recibe llamadas de notificación de eventos salientes desde el copaper después de que el receptor esté conectado correctamente al cliente a una instancia de copaper. El cliente realiza la conexión mediante un objeto de punto de conexión administrado por el copaper. Puede haber numerosos puntos de conexión en un único objeto COM conectable. En el ejemplo **StoServe** , el copaper tiene solo un punto de conexión, que controla los eventos de papel del dibujo.

Cualquier número de clientes puede conectarse a un único punto de conexión. El \_ punto de conexión de CONNPOINT PAPERSINK del copaper mantiene un grupo de conexiones que pueden crecer dinámicamente en tiempo de ejecución. Los detalles completos sobre la compatibilidad con objetos conectables de copapers se codifican en archivos CONNECT. H y CONNECT. CPP y no se tratarán aquí. La construcción es muy similar a la que se estudió en el ejemplo de conservación de código.

El cliente de **StoClien** implementa los objetos de receptor adecuados para los puntos de conexión que espera encontrar en el copaper. En el contexto de copaper, el objeto receptor importante que implementa **StoClien** expone la interfaz **IPaperSink** . Esta es la interfaz de salida utilizada por el copaper para notificar a **StoClien** de varios eventos en el copaper.

A continuación se muestra un resumen de los métodos de **IPaperSink** de IPAPER. H en el \\ directorio del mismo nivel.



| Método   | Descripción                                                   |
|----------|---------------------------------------------------------------|
| Bloqueado   | Un cliente ha tomado el control del documento y lo ha bloqueado.           |
| Desbloqueado | Un cliente ha renunciado al control del papel.               |
| Cargado   | Un cliente ha cargado el contenido de papel de su propio archivo compuesto. |
| Guardado    | Un cliente ha guardado el contenido del papel en su propio archivo compuesto.    |
| InkStart | Un cliente ha iniciado una secuencia de dibujo de tinta de color en el papel.   |
| InkDraw  | Un cliente está colocando puntos de datos de tinta en la superficie del papel.     |
| InkStop  | Un cliente ha detenido la secuencia de dibujo de tinta al papel.   |
| Borrar   | Un cliente borró todos los datos de tinta del papel.              |
| Tamaño  | Un cliente ha cambiado el tamaño del papel.                               |



 

Estos métodos se explican por sí solos. Aunque el receptor debe implementar todos estos métodos de alguna manera, muchos se implementan como código auxiliar y no se usan en los ejemplos de StoClien de **StoServe** /  .

Un método importante que se usa en estos ejemplos es el método cargado. Cuando el cliente indica el copapel para cargar un nuevo dibujo desde el archivo, necesita una manera de notificar al cliente cuando se cargan los nuevos datos. Para ello, el copaper llama a **IPaperSink:: Loaded** en el receptor de cliente. A continuación, el cliente puede llamar a [**IPaper:: redraw**](ipaper--redraw.md) para solicitar que el papel reproduzca los nuevos datos en el cliente. Volver a dibujar hace que el dibujo cargado en la pantalla del cliente se vuelva a dibujar. Una vez completada la carga, el dibujo recién cargado se muestra automáticamente en la ventana proporcionada por el cliente.

Vea [**IPaper:: redraw**](ipaper--redraw.md) para obtener información completa sobre la conectividad de este método IPaper a **IPaperSink**.

Los  métodos IPaperSink **InkStart**, **InkDraw** y **InkStop** se usan para enviar paquetes de datos de tinta individuales de vuelta al cliente. En la recepción, el cliente los pinta en su pantalla de la misma manera que cuando los envió originalmente a un copaper. La lógica anterior es lo suficientemente general como para permitir que varios clientes que están escuchando en el mismo \_ punto de conexión de CONNPOINT PAPERSINK. Si estos clientes comparten una instancia de copaper común, todas podrían mostrar el mismo dibujo conectándose a este punto de conexión.

 

 