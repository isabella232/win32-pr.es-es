---
title: Control de errores con funciones DE MIDI
description: Control de errores con funciones DE MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Interfaz digital instrumentable (MIDI), errores
- MIDI (Interfaz digital de instrumentar música), errores
- servicios DE MIDI, errores
- Errores de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370843"
---
# <a name="handling-errors-with-midi-functions"></a>Control de errores con funciones DE MIDI

Las funciones de audio MIDI devuelven un código de error distinto de cero. Para los errores asociados a MIDI, las [**funciones midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) y [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperan descripciones textuales de los códigos de error. La aplicación debe seguir observando el propio valor de error para determinar cómo continuar, pero puede usar las descripciones de errores en los cuadros de diálogo para informar a los usuarios de las condiciones de error.

Las únicas funciones de MIDI que no devuelven códigos de error son las funciones [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) y [**midiOutGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) Estas funciones devuelven un valor de cero si no hay ningún dispositivo en un sistema o si la función encuentra algún error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 