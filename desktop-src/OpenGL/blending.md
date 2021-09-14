---
title: Mezcla
description: La combinación combina los valores R, G, B y A de un fragmento con los almacenados en el búfer de fotogramas en la ubicación correspondiente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Canalización de procesamiento de OpenGL, combinación
- combinar OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161137"
---
# <a name="blending"></a>Mezcla

La combinación combina los valores R, G, B y A de un fragmento con los almacenados en el búfer de fotogramas en la ubicación correspondiente. La combinación, que solo se realiza en modo RGBA, depende del valor alfa del fragmento y del píxel almacenado actualmente correspondiente; también puede depender de los valores RGB. Puede controlar la combinación con [**glBlendFunc**](glblendfunc.md), con la que se indican los factores de combinación de origen y destino.

 

 




