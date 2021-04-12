---
title: El método IOleContainer EnumObjects
description: El método IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268361"
---
# <a name="the-iolecontainerenumobjects-method"></a>El método IOleContainer:: EnumObjects

Este método se utiliza para enumerar todos los objetos OLE contenidos en un documento o formulario, devolviendo un puntero de interfaz para cada objeto OLE. El contenedor debe devolver punteros a cada objeto OLE que comparta el mismo contenedor. También se deben enumerar los formularios anidados o los controles anidados.

Algunos contenedores implementan controles extensores, que encapsulan controles que no son de ActiveX y, a continuación, devuelven punteros a estos controles extensores a medida que se enumera un formulario. Este comportamiento permite que los controles ActiveX y los contenedores de controles ActiveX se integren bien con controles no ActiveX y, por tanto, se recomienda, pero no es necesario.

 

 




