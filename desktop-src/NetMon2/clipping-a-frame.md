---
description: Puede especificar que el controlador recorte los fotogramas.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recorte de un marco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9251fc6f8a1c9612a9fa7301ea8948956291ad0d074f90ff2ccbbf3f799bd2b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911265"
---
# <a name="clipping-a-frame"></a>Recorte de un marco

Puede especificar que el controlador recorte los fotogramas. (Si se omiten las otras secciones del filtro de captura, esta puede ser la única función del filtro de captura). Si el **campo nFrameBytesToCopy** no es cero (0), su valor especifica cuántos bytes de cada fotograma se reciben para conservar. Si el campo es cero, se conserva todo el marco.

> [!Note]  
> Puede recortar cualquier fotograma que pase las demás partes del filtro de captura estableciendo **nFrameBytesToCopy**.

 

 

 



