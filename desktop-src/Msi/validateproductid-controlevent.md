---
description: El evento ValidateProductID establece la propiedad ProductID en el identificador de producto completo. Si la validación no se realiza correctamente, este evento coloca un mensaje de error y un cuadro de diálogo modal para una entrada de usuario del id. de producto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae9ae5747deb9995c2e33a5c44541793442be8844b224c28c8a91e412cb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786665"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent

El evento ValidateProductID establece la [**propiedad ProductID**](productid.md) en el identificador de producto completo. Si la validación no se realiza correctamente, este evento coloca un mensaje de error y un cuadro de diálogo modal para una entrada de usuario del id. de producto.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario niveles](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) de un cuadro de diálogo modal está asociado a este evento y se usa para comprobar la entrada del usuario del id. de producto. Si la entrada del usuario es válida, se abrirá el siguiente cuadro de diálogo.

 

 



