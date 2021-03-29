---
description: TSPIMessage es un tipo de enumeración que define el conjunto de funciones LINEEVENT y PHONEEVENT adicionales que aparecen en TSPI que no aparecen en TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811438"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage** es un tipo de enumeración que define el conjunto de funciones [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) y [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) adicionales que aparecen en TSPI que no aparecen en TAPI.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base de mensaje de TSPI \_
</dt> <dd>

El número más bajo del intervalo de valores de mensaje específicos de TSPI. Este valor no tiene ningún significado por sí solo, pero sirve como base para definir los demás valores.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LÍNEA \_ NEWCALL
</dt> <dd>

Especifica que ha llegado una nueva llamada entrante y la introduce en TAPI. Este debe ser el primer mensaje enviado a TAPI para una nueva llamada entrante. TAPI devuelve su identificador opaco para la llamada como parte de su control de este mensaje.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LÍNEA \_ CALLDEVSPECIFIC
</dt> <dd>

Especifica que se ha producido un evento específico del dispositivo en un dispositivo de llamada.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LÍNEA \_ CALLDEVSPECIFICFEATURE
</dt> <dd>

Especifica que se ha producido un evento de característica específico del dispositivo en un dispositivo de llamada.

</dd> </dl>

 

 
