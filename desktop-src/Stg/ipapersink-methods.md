---
title: Métodos IPaperSink
description: COPaper expone la interfaz IConnectionPointContainer para que los clientes puedan conectarse a COPaper con el fin de recibir notificaciones de eventos especificados que se producen en COPaper.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf83c3b4bb5c043b02e05324521ea2a4e5783fe4ef959487d83a2607851b533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961355"
---
# <a name="ipapersink-methods"></a>Métodos IPaperSink

COPaper expone la interfaz [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) para que los clientes puedan conectarse a COPaper con el fin de recibir notificaciones de eventos especificados que se producen en COPaper. Al exponer esta interfaz, COPaper se convierte en un objeto conectable. Un cliente puede llamar [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para esta interfaz y usarla para obtener los puntos de conexión del objeto. La participación del cliente en este esquema se trata en el **ejemplo de StoClien** asociado.

Básicamente, el cliente implementa lo que se denomina receptor en forma de un objeto receptor con una interfaz de receptor. La interfaz receptora recibe llamadas de notificación de eventos salientes de COPaper después de que el cliente conecte correctamente el receptor a una instancia de COPaper. El cliente realiza la conexión mediante un objeto de punto de conexión administrado por COPaper. Puede haber numerosos puntos de conexión en un único objeto COM conectable. En el **ejemplo de StoServe,** COPaper tiene solo un punto de conexión, que controla los eventos de dibujo en papel.

Cualquier número de clientes puede conectarse a un único punto de conexión. El punto de conexión CONNPOINT PAPERSINK de COPaper mantiene un grupo de conexiones que pueden crecer \_ dinámicamente en tiempo de ejecución. Los detalles completos sobre la compatibilidad con objetos conectables de COPaper se codifican en los archivos CONNECT. H y CONNECT. CPP y no se tratarán aquí. La construcción es muy similar a la que se ha estudiado en el ejemplo de código CONSERVE.

El **cliente de StoClien** implementa los objetos receptores adecuados para los puntos de conexión que espera encontrar en COPaper. Desde el contexto de COPaper, el importante objeto receptor que **Implementa StoClien** expone la **interfaz IPaperSink.** Esta es la interfaz saliente que usa COPaper para notificar a **StoClien** de varios eventos en COPaper.

Este es un resumen de los métodos de **IPaperSink** de IPAPER. H en el \\ directorio relacionado de INC.



| Método   | Descripción                                                   |
|----------|---------------------------------------------------------------|
| Bloqueado   | Un cliente ha tomado el control del papel y lo ha bloqueado.           |
| Desbloqueado | Un cliente ha cedido el control del documento.               |
| Cargado   | Un cliente ha cargado contenido de papel desde su propio archivo compuesto. |
| Guardado    | Un cliente ha guardado contenido de papel en su propio archivo compuesto.    |
| InkStart | Un cliente inició una secuencia de dibujo de lápiz de color en el papel.   |
| InkDraw  | Un cliente coloca puntos de datos de entrada de lápiz en la superficie del papel.     |
| InkStop  | Un cliente ha detenido su secuencia de dibujo de lápiz en el papel.   |
| Borrado   | Un cliente ha borrado todos los datos de entrada de lápiz del papel.              |
| Redimensionada  | Un cliente ha cambiado el tamaño del papel.                               |



 

Estos métodos se explican en gran medida por sí solos. Aunque el receptor debe implementar todos estos métodos de alguna manera, muchos se implementan como código auxiliar y no se usan en los ejemplos **de StoServe** / **StoClien.**

Un método importante que se usa en estos ejemplos es el método Loaded. Cuando el cliente le dice a COPaper que cargue un nuevo dibujo desde el archivo, necesita una manera de notificar al cliente cuando se cargan los nuevos datos. Para ello, COPaper llama **a IPaperSink::Loaded** en el receptor del cliente. A continuación, el cliente puede llamar [**a IPaper::Redraw**](ipaper--redraw.md) para solicitar que COPaper reproteja los nuevos datos al cliente. Volver a dibujar hace que se vuelva a dibujar el dibujo cargado en la pantalla del cliente. Cuando se completa la carga, el dibujo recién cargado se muestra automáticamente en la ventana proporcionada por el cliente.

Vea [**IPaper::Redraw**](ipaper--redraw.md) para obtener información completa de la conectividad de este método IPaper a **IPaperSink.**

Los **métodos IPaperSink** **InkStart,** **InkDraw** y **InkStop** se usan para enviar paquetes de datos de entrada de lápiz individuales al cliente. En la recepción, el cliente los pinta en su pantalla de la misma manera que cuando originalmente los envió a COPaper. La lógica anterior es lo suficientemente general como para permitir que varios clientes que escuchan en el mismo punto de conexión CONNPOINT \_ PAPERSINK. Si estos clientes comparten una instancia común de COPaper, todos podrían mostrar el mismo dibujo conectándose a este punto de conexión.

 

 