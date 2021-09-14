---
description: Los terminales de archivo se pueden usar de dos maneras.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Uso de terminales de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073459"
---
# <a name="using-file-terminals"></a>Uso de terminales de archivo

Los terminales de archivo se pueden usar de dos maneras. El método más sencillo consiste en usar [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) para seleccionar un terminal de archivo (reproducción o grabación) en un objeto de llamada TAPI. En este caso, TAPI se encarga de conectar las secuencias de audio a los terminales de pista.

El segundo método permite que una aplicación tenga un control más preciso sobre la asignación de secuencias de audio a pistas. En este escenario, la aplicación enumera las secuencias disponibles en la llamada, elige las que quiere grabar (o usar para la reproducción), crea (o busca para reproducción) las pistas correspondientes en el terminal de archivos y selecciona las pistas en las secuencias de llamada.

Para obtener más información, vea los temas siguientes:

-   [Reproducción simple](simple-playback.md)
-   [Reproducción controlada por seguimiento](track-controlled-playback.md)
-   [Registro simple](simple-record.md)
-   [Registro controlado por seguimiento](track-controlled-record.md)

 

 



