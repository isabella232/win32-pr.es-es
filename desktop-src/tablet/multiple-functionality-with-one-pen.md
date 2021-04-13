---
description: Un lápiz de Tablet PC puede tener más de un extremo que puede interactuar con el digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Varias funciones con un lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361575"
---
# <a name="multiple-functionality-with-one-pen"></a>Varias funciones con un lápiz

Un lápiz de Tablet PC puede tener más de un extremo que puede interactuar con el digitalizador. Si los dos extremos del lápiz pueden generar eventos, se puede usar un extremo para establecer la tinta, seleccionar y apuntar, y el otro extremo se puede usar para otras funciones como el borrado.

Para implementar esta funcionalidad, la aplicación debe poder determinar qué extremo del lápiz se está usando y, por lo tanto, Cuándo cambiar la apariencia del cursor. Para ello, puede buscar el estado de la propiedad [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

Para obtener detalles específicos sobre el uso de la parte posterior del lápiz para borrar, vea [borrar la entrada manuscrita con el lápiz](erasing-ink-with-the-pen.md). Además, el [ejemplo de borrado de tinta](ink-erasing-sample.md) muestra cómo usar la parte posterior del lápiz para borrar la entrada manuscrita.

 

 



