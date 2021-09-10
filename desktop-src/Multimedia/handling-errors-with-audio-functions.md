---
title: Control de errores con funciones de audio
description: Control de errores con funciones de audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimedia, errores de audio de forma de onda
- audio, errores de audio de forma de onda
- audio multimedia, errores de audio auxiliares
- audio, errores de audio auxiliares
- audio de forma de onda, errores
- audio auxiliar, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371287"
---
# <a name="handling-errors-with-audio-functions"></a>Control de errores con funciones de audio

Las funciones audio-forma de onda y audio auxiliar devuelven un valor distinto de cero cuando se produce un error. Windows proporciona funciones que convierten estos valores de error en descripciones textuales de los errores. La aplicación todavía debe examinar los valores de error para determinar cómo continuar, pero se pueden usar descripciones textuales de errores en cuadros de diálogo que describen los errores a los usuarios.

Puede usar las siguientes funciones para recuperar descripciones textuales de valores de error de audio:



| Función                                           | Descripción                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Recupera una descripción textual de un error de entrada de audio de forma de onda especificado.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Recupera una descripción textual de un error de salida de audio de forma de onda especificado. |



 

Las únicas funciones de audio que no devuelven valores de error son [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)y [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs). Estas funciones devuelven cero si no hay ningún dispositivo en un sistema o si encuentran errores.

 

 