---
description: En este tema se proporciona un procedimiento para realizar la grabación controlada por seguimiento de secuencias de audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499c4cb79015effa80add4fc5369ec53f134e83f3f1b7e4cda06b09869c01386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872675"
---
# <a name="track-controlled-record"></a>Track-Controlled registro

En este tema se proporciona un procedimiento para realizar la grabación controlada por seguimiento de secuencias de audio.

**Para realizar una grabación controlada por seguimiento de secuencias de audio**

1.  Seleccione Terminales de seguimiento de archivos en secuencias.
2.  Cree el Terminal de registro de archivos.
3.  Establezca el nombre de archivo.
4.  Enumerar secuencias en la llamada TAPI. Para estos pasos, consulte el procedimiento siguiente.
5.  Llame al [**método Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el Terminal de registro de archivos para iniciar la grabación de secuencias.

**Para enumerar secuencias en la llamada TAPI**

1.  Cree una pista del mismo tipo de audio y dirección que la secuencia.
2.  Establezca las propiedades de la pista para el formato de audio. Si no se establece, el formato será el mismo que el formato de secuencias.
3.  Seleccione la pista en la secuencia.

Si se selecciona una pista en varias secuencias, esto implica mezclar secuencias.

 

 



