---
description: Obtenga información sobre las funciones que se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funciones de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394860"
---
# <a name="asynchronous-printing-notification-functions"></a>Funciones de notificación de impresión asincrónica

Las siguientes funciones se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el cola de impresión, como controladores de impresora y monitores de puerto.

## <a name="in-this-section"></a>En esta sección



| Función                                                                                        | Descripción                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Crea un canal de comunicación entre un componente de impresión hospedado en Administrador de trabajos de impresión, como un controlador de impresión o un monitor de puerto, y una aplicación que recibe notificaciones del componente.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Permite que una aplicación se registre para recibir notificaciones de los componentes de impresión hospedados en El cola de impresión, como controladores de impresora, procesadores de impresión y monitores de puerto.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Permite que una aplicación que se ha registrado reciba notificaciones de los componentes de impresión hospedados por el cola de impresión para anular el registro.<br/>                                                              |



 

 

 




