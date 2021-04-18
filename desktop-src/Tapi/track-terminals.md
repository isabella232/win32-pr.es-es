---
description: Se definen dos tipos de terminales de seguimiento que realizan el seguimiento de terminal y de pista de reproducción, que pertenecen respectivamente a y se administran mediante el terminal de grabación de archivos y el terminal de reproducción de archivos.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Seguimiento de terminales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688094"
---
# <a name="track-terminals"></a>Seguimiento de terminales

Se definen dos tipos de terminales de seguimiento: seguimiento de la pista de terminal y reproducción de pista, que, respectivamente, pertenecen a y se administran mediante terminal de grabación de archivos y terminal de reproducción de archivos.

Todos los terminales de seguimiento exponen las interfaces [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) y [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . La interfaz **ITTerminal** permite seleccionar terminales de seguimiento en flujos o llamadas.

> [!Note]  
> El seguimiento de los terminales también expone una interfaz privada, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), que usa el MSP. Las aplicaciones no deben intentar tener acceso a esta interfaz.

 

 

 
