---
title: Controlador predeterminado y controladores personalizados
description: Controlador predeterminado y controladores personalizados
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994051"
---
# <a name="the-default-handler-and-custom-handlers"></a>Controlador predeterminado y controladores personalizados

La mayoría de las aplicaciones usan el controlador predeterminado, una implementación proporcionada por OLE, como controlador. Una aplicación implementa un controlador personalizado cuando las capacidades del controlador predeterminado son insuficientes. Un controlador personalizado puede reemplazar por completo el controlador predeterminado o usar partes de la funcionalidad que proporciona cuando corresponda. En el último caso, el controlador de la aplicación se implementa como un objeto agregado compuesto por un nuevo objeto de control y por el controlador predeterminado. Los controladores predeterminados o de aplicación combinados también se conocen como *controladores en proceso*. El *controlador de comunicación remota* se utiliza para los objetos que no tienen asignado un CLSID en el registro del sistema o que no tienen un controlador especificado. Todo lo que se necesita de un controlador para estos tipos de objetos es que pasan información a través del límite del proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de objetos](object-handlers.md)
</dt> </dl>

 

 




