---
title: Coherencia de transferencia de archivos
description: BITS garantiza que la versión del archivo que transfiere es coherente en función del tamaño del archivo y la marca de tiempo, no del contenido (BITS no protege contra ataques de tipo "Man in the middle").
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608566f6e9927fdcb39133c30720a46ead869f36d3084c950b9ed86379c4b749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959504"
---
# <a name="file-transfer-consistency"></a>Coherencia de transferencia de archivos

BITS garantiza que la versión del archivo que transfiere es coherente en función del tamaño del archivo y la marca de tiempo, no del contenido (BITS no protege contra ataques de tipo "Man in the middle"). Para comprobar el contenido, puede usar el método [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) para obtener el nombre del archivo que contiene el contenido descargado, comprobar el contenido mediante su propio mecanismo y, a continuación, llamar al método [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) para indicar a BITS si el contenido del archivo es válido. Si establece el estado de validación en **FALSE** y el contenido es del servidor de origen, el trabajo entra en el estado de error. Si el contenido es de un elemento del mismo nivel, BITS descarga el archivo desde el servidor de origen.

En el caso de las descargas, si el tamaño del archivo o la marca de tiempo cambian mientras BITS transfiere el archivo, BITS reinicia la transferencia de ese archivo solo. Por ejemplo, si el trabajo de descarga contiene dos archivos y los archivos se actualizan en el servidor mientras BITS transfiere el segundo archivo, BITS reinicia solo la transferencia del segundo archivo. El primer archivo, que ya se ha transferido correctamente, no se actualiza para reflejar los nuevos cambios.

Tenga en cuenta que si es el propietario del archivo que se descarga desde el servidor, debe crear una nueva dirección URL para cada nueva versión del archivo. Si usa la misma dirección URL para las nuevas versiones del archivo, algunos servidores proxy pueden servir datos obsoletos de su caché porque no comprueban con el servidor original si el archivo está obsoleto.

En el caso de las cargas, si el tamaño del archivo o la marca de tiempo cambian durante la transferencia de archivos, BITS genera un error y el trabajo se coloca en el estado BG \_ JOB \_ STATE \_ ERROR.

BITS no sincroniza las solicitudes de transferencia cuando uno o varios usuarios solicitan que el mismo archivo se transfiera a la misma ubicación. BITS transfiere el archivo para cada solicitud por separado.

 

 




