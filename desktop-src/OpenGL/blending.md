---
title: Mezcla
description: La combinación combina los valores R, G, B y A de un fragmento con los almacenados en el búfer de fotogramas en la ubicación correspondiente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Canalización de procesamiento de OpenGL, combinación
- blending OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b38786d2320a646bd6cac096e535e4e1441df98522ac86a146836b929c0986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361439"
---
# <a name="blending"></a>Mezcla

La combinación combina los valores R, G, B y A de un fragmento con los almacenados en el búfer de fotogramas en la ubicación correspondiente. La mezcla, que solo se realiza en modo RGBA, depende del valor alfa del fragmento y del píxel almacenado actualmente correspondiente; también puede depender de los valores RGB. Puede controlar la mezcla con [**glBlendFunc,**](glblendfunc.md)con la que se indican los factores de combinación de origen y destino.

 

 




