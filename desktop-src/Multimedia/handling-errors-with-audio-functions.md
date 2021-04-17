---
title: Control de errores con funciones de audio
description: Control de errores con funciones de audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimedia, errores de audio de onda
- audio, errores de audio de onda
- audio multimedia, errores de audio auxiliar
- audio, errores de audio auxiliar
- audio de la onda, errores
- audio auxiliar, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358857"
---
# <a name="handling-errors-with-audio-functions"></a>Control de errores con funciones de audio

Las funciones de audio de onda y de audio auxiliar devuelven un valor distinto de cero cuando se produce un error. Windows proporciona funciones que convierten estos valores de error en descripciones textuales de los errores. La aplicación debe seguir examinando los valores de error para determinar cómo proceder, pero se pueden usar descripciones de texto de los errores en los cuadros de diálogo que describen los errores para los usuarios.

Puede utilizar las siguientes funciones para recuperar descripciones textuales de los valores de error de audio:



| Función                                           | Descripción                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Recupera una descripción textual de un error de entrada de audio de onda especificada.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Recupera una descripción textual de un error de salida de onda de audio especificado. |



 

Las únicas funciones de audio que no devuelven valores de error son [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)y [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs). Estas funciones devuelven cero si no hay ningún dispositivo presente en un sistema o si encuentran errores.

 

 