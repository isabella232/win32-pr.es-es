---
description: El léxico, o lista de posibles palabras usadas por el modelo de lenguaje de un reconocedor determinado, se encuentra en uno o varios diccionarios.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Diccionarios y listas de frases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cc5b97918e1fed384494e887b604f1d08856e27232ed82f09bceff3ce14fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110965"
---
# <a name="dictionaries-and-phrase-lists"></a>Diccionarios y listas de frases

El léxico, o lista de posibles palabras usadas por el modelo de lenguaje de un reconocedor determinado, se encuentra en uno o varios diccionarios. El reconocedor busca en todos los diccionarios disponibles en el sistema al compilar coincidencias de reconocimiento. Puede usar Microsoft Speech API (SAPI) para modificar algunos de estos diccionarios.

Una lista de frases proporciona otro medio para modificar el vocabulario del reconocedor. Agregar palabras a una lista de frases amplía el vocabulario; Agregar palabras y, a continuación, restringir el reconocedor para usar solo la lista de frases (en lugar de la lista de frases y los diccionarios) restringe el vocabulario.

Las versiones anteriores de tablet PC Technology API se basaban en el concepto de listas de palabras. Las listas de palabras son casi idénticas a las listas de frases y se usan para el mismo propósito cuando se trabaja directamente con un objeto [**RecognizerContext**](inkrecognizercontext-class.md) en una aplicación habilitada para la entrada de lápiz. Para obtener más información sobre dónde y cuándo usar listas de palabras, vea [Establecer contexto para Ink-Enabled controles](setting-context-for-ink-enabled-controls.md).

Cuando el tamaño de la lista con la que desea ampliar el léxico supera las 100 000 palabras, se recomienda usar un diccionario en lugar de una lista de palabras o una lista de frases.

 

 



