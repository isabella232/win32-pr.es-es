---
description: Opcional Secuencias
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Opcional Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362382"
---
# <a name="optional-streams"></a>Opcional Secuencias

Un DMO puede designar algunos de sus flujos de salida como opcionales. Una secuencia opcional genera datos que la aplicación puede descartar, ya sea por completo o en muestras ocasionales. Por ejemplo, una secuencia opcional podría contener información adicional sobre una secuencia principal.

Para consultar si una secuencia es opcional, llame al método [**IMediaObject::GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) y compruebe el *parámetro pdwFlags.* Las secuencias opcionales devuelven la DMO OUTPUT STREAMF DISCARDABLE o la \_ \_ DMO OUTPUT \_ \_ \_ STREAMF \_ OPTIONAL. Estas marcas significan casi lo mismo; en breve se explicará una pequeña diferencia entre ellos.

Si una secuencia es opcional, el cliente puede indicar al DMO que descarte los datos de esa secuencia cuando procese la salida. Para ello, llame al método [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) y establezca el búfer de salida en **NULL** para cada secuencia que quiera descartar. (El búfer de salida se especifica en el **miembro pBuffer** del DMO [**OUTPUT DATA \_ \_ \_ BUFFER).**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) Establezca también la DMO \_ PROCESS OUTPUT DISCARD WHEN NO BUFFER en el parámetro \_ \_ \_ \_ \_ *dwFlags.*

Para cada secuencia en la que *el puntero pBuffer* es **NULL,** el DMO intentará descartar los datos. Si la secuencia es opcional, se garantiza DMO la secuencia descartará los datos. Si la secuencia no es opcional, el DMO descarta los datos cuando sea posible, pero no se garantiza que lo haga. Si no puede descartar los datos, establece la marca \_ DMO OUTPUT \_ DATA \_ BUFFERF \_ INCOMPLETE. Si establece un puntero *pBuffer* en **NULL** pero no establece la marca DMO PROCESS OUTPUT DISCARD WHEN NO BUFFER, el DMO no descarta \_ los \_ \_ \_ \_ \_ datos. En ese caso, el DMO almacena en búfer la salida internamente o simplemente produce un error en la **llamada a ProcessOutput.**

La única diferencia funcional entre la DMO OUTPUT STREAMF OPTIONAL y la DMO \_ \_ OUTPUT \_ \_ \_ STREAMF \_ DISCARDABLE es la siguiente:

-   La DMO OUTPUT STREAMF OPTIONAL indica que el cliente no tiene que establecer un tipo \_ de medio en esa \_ \_ secuencia. Sin embargo, si el cliente comienza a procesar datos sin establecer el tipo de medio para esa secuencia, debe descartar los datos de esa secuencia durante todo el streaming. Si desea descartar muestras de forma selectiva, debe establecer el tipo de medio.
-   La DMO OUTPUT STREAMF DISCARDABLE indica que, aunque la secuencia es \_ \_ \_ opcional, siempre requiere un tipo de medio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedaje directo de un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



