---
title: Control de errores con funciones MIDI
description: Control de errores con funciones MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Interfaz digital de instrumentar música (MIDI), errores
- MIDI (Interfaz digital de instrumentar música), errores
- servicios DE MIDI, errores
- Errores de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062912"
---
# <a name="handling-errors-with-midi-functions"></a>Control de errores con funciones MIDI

Las funciones de audio MIDI devuelven un código de error distinto de cero. En el caso de los errores asociados a MIDI, las funciones [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) y [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperan descripciones textuales de los códigos de error. La aplicación todavía debe mirar el propio valor de error para determinar cómo continuar, pero puede usar las descripciones de errores en los cuadros de diálogo para informar a los usuarios de las condiciones de error.

Las únicas funciones de MIDI que no devuelven códigos de error son las funciones [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) y [**midiOutGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) Estas funciones devuelven un valor de cero si no hay ningún dispositivo en un sistema o si la función encuentra algún error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 