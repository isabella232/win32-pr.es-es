---
title: StopAll (método)
description: StopAll (método)
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704937"
---
# <a name="stopall-method"></a>StopAll (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Detiene todas las solicitudes de animación o los tipos de solicitudes especificados para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). StopAll*( *  \[ *tipo* )\]



| Parte   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type* | Opcional. Para usar este parámetro, puede usar cualquiera de los siguientes valores. También puede especificar varios tipos separándolos con comas. <br/> "**Obtener**" <br/> Para detener todas las solicitudes [**Get**](get-method.md) en cola.<br/> "**NonQueuedGet**" <br/> Para detener todas las solicitudes [**Get**](get-method.md) no en cola (método **Get** con el parámetro **Queue** establecido en **false**).<br/> "**Movimiento**" <br/> Para detener todas las solicitudes en cola [**moveTo**](moveto-method.md) .<br/> "**Reproducir**" <br/> Para detener todas las solicitudes de [**reproducción**](play-method.md) en cola.<br/> "**Hablar**" <br/> Para detener todas las solicitudes de [**voz**](speak-method.md) en cola.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si no establece el parámetro de **tipo** , el servidor detiene todas las animaciones para el carácter, incluidas las solicitudes [**Get**](get-method.md) en cola y no en cola, y borra su cola de animaciones. También detiene la reproducción de la animación que oculta o muestra un carácter.

Este método no generará un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Consulte también

[**Método Stop**](stop-method.md)


 

