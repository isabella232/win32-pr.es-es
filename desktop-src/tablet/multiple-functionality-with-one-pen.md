---
description: Un lápiz de Tablet PC puede tener más de un extremo que pueda interactuar con el digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Funcionalidad múltiple con un lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574465"
---
# <a name="multiple-functionality-with-one-pen"></a>Funcionalidad múltiple con un lápiz

Un lápiz de Tablet PC puede tener más de un extremo que pueda interactuar con el digitalizador. Si ambos extremos del lápiz pueden generar eventos, se puede usar un extremo para establecer la entrada de lápiz, seleccionar y apuntar, y el otro extremo se puede usar para otras funciones, como el borrado.

Para implementar dicha funcionalidad, la aplicación debe ser capaz de determinar qué extremo del lápiz se está utilizando y, por tanto, cuándo cambiar la apariencia del cursor. Para ello, busque el estado de la [**propiedad Invertido**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el [**objeto Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

Para obtener detalles específicos sobre el uso de la parte posterior del lápiz para borrar, vea Borrar la entrada [manuscrita con el lápiz](erasing-ink-with-the-pen.md). Además, el [ejemplo de borrado de lápiz](ink-erasing-sample.md) muestra cómo usar la parte posterior del lápiz para borrar la entrada de lápiz.

 

 



