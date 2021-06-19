---
description: Obtenga información sobre las interfaces que se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396100"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfaces de notificación de impresión asincrónica

Las interfaces siguientes se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión, como controladores de impresora y monitores de puerto.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                     | Descripción                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crea y administra un canal de comunicación utilizado por las aplicaciones y los componentes hospedados por el cola de impresión.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Representa un canal de comunicación que los componentes hospedados por el colador de impresión usan para enviar notificaciones a las aplicaciones. Si el canal es bidireccional, las aplicaciones pueden usar el mismo canal para enviar respuestas de vuelta al componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Encapsula los datos enviados en un canal de notificación. <br/>                                                                                                                                                                                             |



 

 

 




