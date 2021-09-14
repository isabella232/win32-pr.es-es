---
title: Método IOleContainer EnumObjects
description: Método IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253106"
---
# <a name="the-iolecontainerenumobjects-method"></a>IOleContainer::EnumObjects (Método)

Este método se usa para enumerar todos los objetos OLE contenidos en un documento o formulario, devolviendo un puntero de interfaz para cada objeto OLE. El contenedor debe devolver punteros a cada objeto OLE que comparta el mismo contenedor. También se deben enumerar los formularios anidados o los controles anidados.

Algunos contenedores implementan controles extensores, que encapsulan controles no ActiveX y, a continuación, devuelven punteros a estos controles extensores a medida que se enumera un formulario. Este comportamiento permite que ActiveX y contenedores de controles ActiveX se integren bien con los controles que no son de ActiveX y, por tanto, se recomienda, pero no es necesario.

 

 




