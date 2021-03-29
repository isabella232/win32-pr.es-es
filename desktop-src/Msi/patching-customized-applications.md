---
description: Al instalar una revisión y una o varias transformaciones de personalización en una aplicación, la revisión suele instalarse primero, seguida de las transformaciones de personalización.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Aplicación de revisiones a aplicaciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360709"
---
# <a name="patching-customized-applications"></a>Aplicación de revisiones a aplicaciones personalizadas

Al instalar una revisión y una o varias transformaciones de personalización en una aplicación, la revisión suele instalarse primero, seguida de las transformaciones de personalización. Por diseño, la revisión no está interrumpida por la instalación posterior de la personalización. Sin embargo, la instalación de las transformaciones primero y, a continuación, la revisión, puede interrumpir la personalización.

Por ejemplo, una interrupción en la personalización podría producirse cuando se usa una revisión para actualizar un producto de la versión 1 a la versión 2 y una transformación de personalización que funciona para la versión 1 no funciona para la versión 2. En este caso, la revisión de actualización de la versión no se puede aplicar a un producto personalizado sin desinstalar primero y, a continuación, volver a instalar el producto original.

 

 



