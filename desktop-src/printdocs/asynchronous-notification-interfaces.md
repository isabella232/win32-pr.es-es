---
description: Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817766"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfaces de notificación de impresión asincrónica

Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                     | Descripción                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crea y administra un canal de comunicación que utilizan las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Representa un canal de comunicación que los componentes hospedados por el administrador de trabajos de impresión usan para enviar notificaciones a las aplicaciones. Si el canal es bidireccional, las aplicaciones pueden usar el mismo canal para devolver respuestas al componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Encapsula los datos enviados en un canal de notificación. <br/>                                                                                                                                                                                             |



 

 

 




