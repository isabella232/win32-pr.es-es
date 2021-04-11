---
description: Una aplicación del visor de eventos utiliza la función OpenEventLog para abrir el registro de eventos de un origen de eventos.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Leer del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082488"
---
# <a name="reading-from-the-event-log"></a>Leer del registro de eventos

Una aplicación del visor de eventos utiliza la función [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para abrir el registro de eventos de un origen de eventos. Después, el visor de eventos puede usar la función [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para leer los registros de eventos del registro. **ReadEventLog** devuelve un búfer que contiene una estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e información adicional que describe un evento registrado. En el siguiente diagrama se muestra este proceso.

![leer del registro de eventos](images/readlog.png)

Para obtener código de ejemplo, consulte [consultar información de eventos](querying-for-event-source-messages.md).

 

 



