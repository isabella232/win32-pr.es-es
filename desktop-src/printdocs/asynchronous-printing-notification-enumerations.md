---
description: Las enumeraciones siguientes se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión, como controladores de impresora y monitores de puerto.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Enumeraciones de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a86082d171fbf76afc4a7f02a9511fc7ad3d118ced1aa2ef4f43f87a2abd111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950735"
---
# <a name="asynchronous-printing-notification-enumerations"></a>Enumeraciones de notificación de impresión asincrónica

Las enumeraciones siguientes se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión, como controladores de impresora y monitores de puerto.

## <a name="in-this-section"></a>En esta sección



| Enumeración                                                                               | Descripción                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | Especifica si la comunicación es bidireccional o unidireccional entre las aplicaciones y los componentes hospedados en la cola de impresión, como los controladores de impresora, los procesadores de impresión y los monitores de puerto.<br/>           |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | Especifica la parte del código de error del **HRESULT** devuelto después de un error de notificación asincrónica.<br/>                                                                                            |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | Especifica si las notificaciones solo irán a las aplicaciones de escucha asociadas al mismo usuario que el remitente hospedado en Print Spooler, o si van a un conjunto más amplio de aplicaciones de escucha.<br/> |



 

 

 




