---
description: Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funciones de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697669"
---
# <a name="asynchronous-printing-notification-functions"></a>Funciones de notificación de impresión asincrónica

Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.

## <a name="in-this-section"></a>En esta sección



| Función                                                                                        | Descripción                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Crea un canal de comunicación entre un componente de impresión hospedado en el administrador de trabajos de impresión, como un controlador de impresión o un monitor de puerto, y una aplicación que recibe notificaciones del componente.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Permite a una aplicación registrarse para recibir notificaciones de los componentes de impresión hospedados en el administrador de trabajos de impresión, como controladores de impresora, procesadores de impresión y monitores de puerto.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Habilita una aplicación que se ha registrado para recibir notificaciones de los componentes de impresión hospedados en el administrador de trabajos de impresión para anular el registro.<br/>                                                              |



 

 

 




