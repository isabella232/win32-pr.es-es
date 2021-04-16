---
title: Control de errores con funciones MIDI
description: Control de errores con funciones MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Interfaz digital de instrumentos musicales (MIDI), errores
- MIDI (interfaz digital de instrumentos musicales), errores
- Servicios MIDI, errores
- Errores de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651376"
---
# <a name="handling-errors-with-midi-functions"></a>Control de errores con funciones MIDI

Las funciones de audio MIDI devuelven un código de error distinto de cero. En el caso de los errores asociados a MIDI, las funciones [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) y [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperan las descripciones textuales de los códigos de error. La aplicación debe seguir examinando el propio valor de error para determinar cómo proceder, pero puede usar las descripciones de error en los cuadros de diálogo para informar a los usuarios de las condiciones de error.

Las únicas funciones MIDI que no devuelven códigos de error son las funciones [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) y [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Estas funciones devuelven un valor de cero si no hay ningún dispositivo presente en un sistema o si la función encuentra algún error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios MIDI](midi-services.md)
</dt> </dl>

 

 