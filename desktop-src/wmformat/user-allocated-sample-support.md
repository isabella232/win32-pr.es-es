---
title: Compatibilidad con ejemplos asignados por el usuario
description: Compatibilidad con ejemplos asignados por el usuario
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows SDK de formato multimedia, compatibilidad de ejemplo asignada por el usuario
- Formato de sistemas avanzados (ASF), compatibilidad de ejemplo asignada por el usuario
- ASF (formato de sistemas avanzados), compatibilidad de ejemplo asignada por el usuario
- compatibilidad de ejemplo asignada por el usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8cba2d20586cc47845d961e5c92a0138a37d5d0db07feb23dbb68dda1b72eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845259"
---
# <a name="user-allocated-sample-support"></a>Compatibilidad con ejemplos asignados por el usuario

En circunstancias normales, tanto el objeto de lector como el objeto de lector sincrónico crean un nuevo objeto de búfer para cada ejemplo entregado a la aplicación. Esto se debe a que el objeto de lectura no tiene forma de saber lo que hace la aplicación con los ejemplos después de obtenerlos. Aunque muchas aplicaciones leen ejemplos solo para representarlos inmediatamente, es posible que algunas aplicaciones necesiten mantener muestras durante mucho tiempo. Por lo tanto, el objeto de lectura no puede reutilizar ninguno de los búferes que asigna; los entrega a la aplicación, que, a continuación, tiene control sobre ellos.

El problema con este enfoque es que un archivo puede contener un gran número de muestras. Si cada uno de ellos requiere que se cree un nuevo objeto de búfer, se desperdicia mucho tiempo de procesador asignando y liberando memoria. En las aplicaciones que tienen en cuenta el tiempo, como los reproductores multimedia, esta sobrecarga puede ser muy perjudicial para el rendimiento.

Para mitigar los problemas de rendimiento de los ejemplos asignados por el lector, tanto el lector como el lector sincrónico admiten ejemplos asignados por el usuario. Para usar ejemplos asignados por la aplicación, el objeto de lectura realiza llamadas a un método de devolución de llamada de asignación de ejemplo que implemente. La lógica que usa la devolución de llamada para entregar búferes al objeto de lectura es totalmente su función. Puede usar un grupo de búferes para todo el archivo o usar varios grupos de búferes, uno para cada salida o secuencia, o cualquier otro esquema que funcione para la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Asignación de búferes para la lectura de archivos**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Características de lectura de archivos**](file-reading-features.md)
</dt> </dl>

 

 




