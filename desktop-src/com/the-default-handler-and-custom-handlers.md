---
title: El controlador predeterminado y los controladores personalizados
description: El controlador predeterminado y los controladores personalizados
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253119"
---
# <a name="the-default-handler-and-custom-handlers"></a>El controlador predeterminado y los controladores personalizados

La mayoría de las aplicaciones usan el controlador predeterminado, una implementación proporcionada por OLE, como controlador. Una aplicación implementa un controlador personalizado cuando las funcionalidades del controlador predeterminado no son suficientes. Un controlador personalizado puede reemplazar completamente el controlador predeterminado o usar partes de la funcionalidad que proporciona cuando corresponda. En el último caso, el controlador de aplicación se implementa como un objeto agregado compuesto por un nuevo objeto de control y el controlador predeterminado. Los controladores de aplicación/predeterminado combinados también se conocen como *controladores en proceso.* El *controlador de comunicación* remota se usa para los objetos a los que no se asigna un CLSID en el Registro del sistema o que no tienen ningún controlador especificado. Todo lo que se necesita de un controlador para estos tipos de objetos es que pasan información a través del límite del proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de objetos](object-handlers.md)
</dt> </dl>

 

 




