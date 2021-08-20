---
title: El controlador predeterminado y los controladores personalizados
description: El controlador predeterminado y los controladores personalizados
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d7c0cbcff81ed8c0aa1e23d4b6713b33943e6ef925a0a22cb06f7102877eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103753"
---
# <a name="the-default-handler-and-custom-handlers"></a>El controlador predeterminado y los controladores personalizados

La mayoría de las aplicaciones usan el controlador predeterminado, una implementación proporcionada por OLE, como controlador. Una aplicación implementa un controlador personalizado cuando las funcionalidades del controlador predeterminado no son suficientes. Un controlador personalizado puede reemplazar completamente el controlador predeterminado o usar partes de la funcionalidad que proporciona cuando corresponda. En el último caso, el controlador de aplicación se implementa como un objeto agregado compuesto por un nuevo objeto de control y el controlador predeterminado. Los controladores de aplicación/predeterminado combinados también se conocen como *controladores en proceso.* El *controlador de comunicación* remota se usa para los objetos a los que no se asigna un CLSID en el Registro del sistema o que no tienen ningún controlador especificado. Todo lo que se requiere de un controlador para estos tipos de objetos es que pasan información a través del límite del proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de objetos](object-handlers.md)
</dt> </dl>

 

 




