---
title: Propiedad Enabled (objeto AudioOutput)
description: Propiedad Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078770"
---
# <a name="enabled-property-audiooutput-object"></a>Propiedad Enabled (objeto AudioOutput)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un valor booleano que indica si está habilitada la salida de audio (hablado).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente * * *. AudioOutput. Enabled**



| Value     | Descripción                               |
|-----------|-------------------------------------------|
| **True**  | Predeterminada La salida de audio oral está habilitada. |
| **False** | La salida de audio hablada está deshabilitada.          |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad refleja la opción reproducir salida de audio en la página salida de la hoja de propiedades del agente (opciones avanzadas de caracteres). Cuando la propiedad [**Enabled**](enabled-property.md) devuelve **true**, el método [**Speak**](speak-method.md) genera una salida de audio si se instala un motor TTS compatible o si se usan archivos de sonido para la salida de voz. Cuando devuelve **false**, significa que la salida de voz no está instalada o que el usuario ha deshabilitado. La configuración de la propiedad se aplica a todos los caracteres del agente y es de solo lectura; solo el usuario puede establecer este valor de propiedad.

## <a name="see-also"></a>Consulte también

[Evento AgentPropertyChange](agentpropertychange-event.md)


 

 




