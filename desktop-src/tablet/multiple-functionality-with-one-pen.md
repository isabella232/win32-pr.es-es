---
description: Un lápiz de Tablet PC puede tener más de un extremo que pueda interactuar con el digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Varias funcionalidades con un solo lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cbba4c95ef215b8ae1e0c94cbe1d43eaceb966fd775284c57a365bbba2f7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449676"
---
# <a name="multiple-functionality-with-one-pen"></a>Varias funcionalidades con un solo lápiz

Un lápiz de Tablet PC puede tener más de un extremo que pueda interactuar con el digitalizador. Si ambos extremos del lápiz pueden generar eventos, se puede usar un extremo para establecer la entrada de lápiz, seleccionar y apuntar, y el otro extremo se puede usar para otras funciones, como el borrado.

Para implementar dicha funcionalidad, la aplicación debe ser capaz de determinar qué extremo del lápiz se está utilizando y, por tanto, cuándo cambiar la apariencia del cursor. Para ello, busque el estado de la [**propiedad Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el [**objeto Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

Para obtener detalles específicos sobre el uso de la parte posterior del lápiz para borrar, vea Borrar la entrada [manuscrita con el lápiz](erasing-ink-with-the-pen.md). Además, el ejemplo [de borrado de](ink-erasing-sample.md) lápiz muestra cómo usar la parte posterior del lápiz para borrar la entrada manuscrita.

 

 



