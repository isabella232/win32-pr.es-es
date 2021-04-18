---
description: El léxico, o la lista de palabras posibles utilizadas por un modelo de lenguaje del reconocedor determinado, se encuentra en uno o varios diccionarios.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Diccionarios y listas de frases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697564"
---
# <a name="dictionaries-and-phrase-lists"></a>Diccionarios y listas de frases

El léxico, o la lista de palabras posibles utilizadas por un modelo de lenguaje del reconocedor determinado, se encuentra en uno o varios diccionarios. El reconocedor busca en todos los diccionarios disponibles en el sistema al compilar las coincidencias de reconocimiento. Puede usar las API de Microsoft Speech (SAPI) para modificar algunos de estos diccionarios.

Una lista de frases proporciona otro medio para modificar el vocabulario del reconocedor. Al agregar palabras a una lista de frases se amplía el vocabulario; al agregar palabras y restringir el reconocedor para que use solo la lista de frases (en lugar de la lista de frases y los diccionarios) se restringe el vocabulario.

Las versiones anteriores de las API de tecnología de Tablet PC se basaban en el concepto de listas de palabras. Las listas de palabras son casi idénticas a las listas de frases y se usan para el mismo propósito cuando se trabaja directamente con un objeto [**RecognizerContext**](inkrecognizercontext-class.md) en una aplicación que tiene habilitada la entrada de lápiz. Para obtener más información sobre dónde y Cuándo usar las listas de palabras, vea [establecer el contexto para los controles de Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Cuando el tamaño de la lista con la que desea extender el léxico supera las 100.000 palabras, se recomienda usar un diccionario en lugar de una lista de palabras o una lista de frases.

 

 



