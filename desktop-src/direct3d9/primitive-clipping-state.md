---
description: Los primitivos que se encuentran parcialmente dentro (o completamente externos) el frustum de vista se pueden recortar para que solo se represente la parte visible de la primitiva.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Estado de recorte primitivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423152"
---
# <a name="primitive-clipping-state-direct3d-9"></a>Estado de recorte primitivo (Direct3D 9)

Los primitivos que se encuentran parcialmente dentro (o completamente externos) el [frustum de vista](viewports-and-clipping.md) se pueden recortar para que solo se represente la parte visible de la primitiva. El recorte reduce la cantidad de trabajo que se realiza solo a las primitivas o partes de un primitivo que serán visibles.

Para usar la canalización para el recorte, establezca el \_ Estado de representación de recorte de D3DRS en **true** (valor predeterminado) para habilitar el recorte o en **false** para deshabilitar el recorte de Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 



