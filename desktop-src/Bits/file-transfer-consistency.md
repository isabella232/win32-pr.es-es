---
title: Coherencia de la transferencia de archivos
description: BITS garantiza que la versión del archivo que transfiere es coherente según el tamaño del archivo y la marca de tiempo, no el contenido (BITS no protege contra ataques de tipo "Man in the Middle").
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903140"
---
# <a name="file-transfer-consistency"></a>Coherencia de la transferencia de archivos

BITS garantiza que la versión del archivo que transfiere es coherente según el tamaño del archivo y la marca de tiempo, no el contenido (BITS no protege contra ataques de tipo "Man in the Middle"). Para comprobar el contenido usted mismo, puede usar el método [**IBackgroundCopyFile3:: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) para obtener el nombre del archivo que contiene el contenido descargado, comprobar el contenido mediante su propio mecanismo y, a continuación, llamar al método [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) para indicar a bits si el contenido del archivo es válido. Si establece el estado de validación en **false** y el contenido procede del servidor de origen, el trabajo entra en el estado de error. Si el contenido procede de un elemento del mismo nivel, BITS descargará el archivo desde el servidor de origen.

En el caso de las descargas, si el tamaño de archivo o la marca de tiempo cambian mientras BITS está transfiriendo el archivo, BITS reinicia la transferencia de ese archivo únicamente. Por ejemplo, si el trabajo de descarga contiene dos archivos y los archivos se actualizan en el servidor mientras BITS está transfiriendo el segundo archivo, BITS reinicia la transferencia del segundo archivo únicamente. El primer archivo, que ya se transfirió correctamente, no se actualiza para reflejar los nuevos cambios.

Tenga en cuenta que si es el propietario del archivo que se está descargando del servidor, debe crear una nueva dirección URL para cada nueva versión del archivo. Si usa la misma dirección URL para las nuevas versiones del archivo, algunos servidores proxy pueden servir datos obsoletos de la memoria caché porque no se comprueban con el servidor original si el archivo está obsoleto.

En el caso de las cargas, si el tamaño de archivo o la marca de tiempo cambian durante la transferencia de archivos, BITS genera un error y el trabajo se coloca en el estado de error de estado de trabajo de BG \_ \_ \_ .

BITS no sincroniza las solicitudes de transferencia cuando uno o varios usuarios solicitan que el mismo archivo se transfiera a la misma ubicación. BITS transfiere el archivo para cada solicitud por separado.

 

 




