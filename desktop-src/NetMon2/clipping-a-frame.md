---
description: Puede especificar que el controlador recorte los fotogramas.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recorte de un fotograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667121"
---
# <a name="clipping-a-frame"></a>Recorte de un fotograma

Puede especificar que el controlador recorte los fotogramas. (Si se omiten las demás secciones del filtro de captura, esta puede ser la única función del filtro de captura). Si el campo **nFrameBytesToCopy** no es cero (0), su valor especifica el número de bytes de cada fotograma recibidos para conservar. Si el campo es cero, se conserva todo el marco.

> [!Note]  
> Puede recortar cualquier fotograma que pase las demás partes del filtro de captura estableciendo **nFrameBytesToCopy**.

 

 

 



