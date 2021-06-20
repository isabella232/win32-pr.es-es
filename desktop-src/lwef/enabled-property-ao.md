---
title: Propiedad Enabled (objeto AudioOutput)
description: Obtenga información sobre la propiedad de objeto AudioOutput habilitada. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407348"
---
# <a name="enabled-property-audiooutput-object"></a>Propiedad Enabled (objeto AudioOutput)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un valor booleano que indica si la salida de audio (hablada) está habilitada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent!". AudioOutput.Enabled**



| Valor     | Descripción                               |
|-----------|-------------------------------------------|
| **True**  | (Valor predeterminado) La salida de audio hablado está habilitada. |
| **False** | La salida de audio hablado está deshabilitada.          |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad refleja la opción Reproducir salida de audio en la página Salida de la hoja de propiedades agente (Opciones avanzadas de caracteres). Cuando la [**propiedad Enabled**](enabled-property.md) devuelve **True**, el método [**Speak**](speak-method.md) genera una salida de audio si está instalado un motor TTS compatible o usa archivos de sonido para la salida hablada. Cuando devuelve **False**, significa que la salida de voz no está instalada o el usuario la ha deshabilitado. La configuración de propiedad se aplica a todos los caracteres del Agente y es de solo lectura; solo el usuario puede establecer este valor de propiedad.

## <a name="see-also"></a>Consulte también

[Evento AgentPropertyChange](agentpropertychange-event.md)


 

 




