---
description: La lista siguiente contiene los métodos CMSPStream llamados por el objeto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Métodos CMSPStream llamados por el objeto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687890"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>CMSPStream métodos públicos llamados por el objeto MSPCall



| Métodos públicos de CMSPStream                                 | Descripción                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Smss**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Lo llama **MSPCall** cuando se crea la secuencia.                                   |
| [**Apagado**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Lo llama **MSPCall** para anular la selección de todos los objetos de terminal y liberar el objeto de llamada. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Lo llama el objeto MSPCall para obtener el estado actual de la secuencia.                   |
| [**HandleTSPData**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | El objeto de llamada derivado puede llamar a este método para permitir que la secuencia controle los comandos de TSP.     |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Lo llama el objeto MSPCall para permitir que el flujo Controle los eventos de gráfico.                     |



 

 

 



