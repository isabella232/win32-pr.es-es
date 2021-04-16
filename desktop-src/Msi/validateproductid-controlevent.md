---
description: El evento ValidateProductID establece la propiedad ProductID en el identificador de producto completo. Si la validación no se realiza correctamente, este evento coloca un mensaje de error y un cuadro de diálogo modal para una entrada de usuario del ID. de producto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677458"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent,

El evento ValidateProductID establece la propiedad [**ProductID**](productid.md) en el identificador de producto completo. Si la validación no se realiza correctamente, este evento coloca un mensaje de error y un cuadro de diálogo modal para una entrada de usuario del ID. de producto.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento y se usa para comprobar la entrada del usuario del ID. del producto. Si la entrada del usuario es válida, se abrirá el siguiente cuadro de diálogo.

 

 



