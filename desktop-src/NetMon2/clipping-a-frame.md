---
description: Puede especificar que el controlador recorte los fotogramas.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recorte de un marco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253898"
---
# <a name="clipping-a-frame"></a>Recorte de un marco

Puede especificar que el controlador recorte los fotogramas. (Si se omiten las otras secciones del filtro de captura, esta puede ser la única función del filtro de captura). Si el **campo nFrameBytesToCopy** no es cero (0), su valor especifica cuántos bytes de cada fotograma se reciben para conservar. Si el campo es cero, se conserva todo el marco.

> [!Note]  
> Puede recortar cualquier fotograma que pase las otras partes del filtro de captura estableciendo **nFrameBytesToCopy.**

 

 

 



