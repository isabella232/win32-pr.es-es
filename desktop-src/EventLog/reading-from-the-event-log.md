---
description: Una aplicación de visor de eventos usa la función OpenEventLog para abrir el registro de eventos de un origen de eventos.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lectura desde el registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d0756ba7d9609bca285ce33d69738984badf7effff8867fc5c3e1943b09145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151545"
---
# <a name="reading-from-the-event-log"></a>Lectura desde el registro de eventos

Una aplicación de visor de eventos usa [**la función OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para abrir el registro de eventos de un origen de eventos. A continuación, el visor de eventos puede usar [**la función ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para leer los registros de eventos del registro. **ReadEventLog** devuelve un búfer que contiene una [**estructura EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e información adicional que describe un evento registrado. En el siguiente diagrama se muestra este proceso.

![leer desde el registro de eventos](images/readlog.png)

Para obtener código de ejemplo, [vea Querying for Event Information](querying-for-event-source-messages.md).

 

 



