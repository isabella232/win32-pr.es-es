---
title: StopAll (método)
description: StopAll (método)
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b138be6ea75135d5ddefdea9e1e5cc120d875ae092478ad3147332720e5a0907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745947"
---
# <a name="stopall-method"></a>StopAll (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Detiene todas las solicitudes de animación o los tipos de solicitudes especificados para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Tipo StopAll_ *  \[ \]



| Parte   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type* | Opcional. Para usar este parámetro, puede usar cualquiera de los valores siguientes. También puede especificar varios tipos si los separa con comas. <br/> "**Get**" <br/> Para detener todas las solicitudes [**Get**](get-method.md) en cola.<br/> "**NonQueuedGet**" <br/> Para detener todas las solicitudes [**Get**](get-method.md) no en cola **(método Get** con el **parámetro Queue** establecido en **False).**<br/> "**Move**" <br/> Para detener todas las solicitudes [**MoveTo en cola.**](moveto-method.md)<br/> "**Reproducir**" <br/> Para detener todas las solicitudes [**de Play**](play-method.md) en cola.<br/> **"Hablar"** <br/> Para detener todas las solicitudes [**speak en**](speak-method.md) cola.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si no establece el parámetro **Type,** el servidor detiene todas las animaciones del carácter, incluidas las solicitudes [**Get**](get-method.md) en cola y no en cola, y borra su cola de animación. También deja de reproducir la animación Ocultar o Mostrar de un carácter.

Este método no generará un [**objeto Request.**](/windows/desktop/lwef/the-request-object)

## <a name="see-also"></a>Consulte también

[**Método Stop**](stop-method.md)


 

