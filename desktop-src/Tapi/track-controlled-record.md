---
description: En este tema se proporciona un procedimiento para realizar grabaciones controladas por seguimiento de secuencias de audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910306"
---
# <a name="track-controlled-record"></a>Track-Controlled registro

En este tema se proporciona un procedimiento para realizar grabaciones controladas por seguimiento de secuencias de audio.

**Para realizar grabaciones controladas por seguimiento de secuencias de audio**

1.  Seleccione Archivo seguimiento de terminales en secuencias.
2.  Cree el terminal del registro de archivos.
3.  Establezca el nombre de archivo.
4.  Enumerar secuencias en la llamada TAPI. Para estos pasos, consulte el procedimiento siguiente.
5.  Llame al método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el terminal del registro de archivos para iniciar la grabación de la secuencia.

**Para enumerar secuencias en la llamada TAPI**

1.  Cree una pista del mismo tipo de audio y dirección que la secuencia.
2.  Establezca las propiedades de seguimiento para el formato de audio. Si no se establece, el formato será el mismo que el formato de las secuencias.
3.  Seleccione la pista en la secuencia.

Si se selecciona una pista en varios flujos, esto implica mezclar flujos.

 

 



