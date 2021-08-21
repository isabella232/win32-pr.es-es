---
description: Los pasos siguientes se realizan para la reproducción controlada por seguimiento.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Track-Controlled reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc26cd1448c712b99a0e61bf94520531c1c592a289d273257c8bc907b266eea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002623"
---
# <a name="track-controlled-playback"></a>Track-Controlled reproducción

Para realizar la reproducción controlada por seguimiento, haga lo siguiente:

-   Seleccione Track Terminals onto streams (Realizar el seguimiento de terminales en secuencias).
-   Cree el terminal de reproducción de archivos.
-   Establecer propiedades: nombre de archivo y tipo de almacenamiento.
-   Con un método en el Terminal de reproducción de archivos, enumere Terminales de seguimiento de archivos.
-   Enumerar secuencias en la llamada TAPI.
-   Seleccione el Terminal de seguimiento de archivos en la secuencia.
-   Llame al [**método Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el Terminal de reproducción de archivos para iniciar la reproducción de datos grabados en las secuencias TAPI.

 

 



