---
title: Compatibilidad de ejemplo asignada por el usuario
description: Compatibilidad de ejemplo asignada por el usuario
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- SDK de Windows Media Format, compatibilidad de ejemplo asignada por el usuario
- Advanced Systems Format (ASF), compatibilidad de ejemplo asignada por el usuario
- ASF (formato de sistemas avanzados), compatibilidad de ejemplo asignada por el usuario
- compatibilidad de ejemplo asignada por el usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075481"
---
# <a name="user-allocated-sample-support"></a>Compatibilidad de ejemplo asignada por el usuario

En circunstancias normales, tanto el objeto lector como el objeto lector sincrónico crean un nuevo objeto de búfer para cada ejemplo entregado a la aplicación. Esto se debe a que el objeto de lectura no tiene forma de saber lo que hace la aplicación con los ejemplos después de que los obtiene. Aunque muchas aplicaciones leen ejemplos solo para representarlas inmediatamente, es posible que algunas aplicaciones necesiten mantener muestras durante mucho tiempo. El objeto de lectura no puede, por consiguiente, volver a usar ninguno de los búferes que asigna; los entrega a la aplicación, que, a su vez, tiene el control sobre ellas.

El problema de este enfoque es que un archivo puede contener un gran número de muestras. Si cada uno de ellos requiere la creación de un nuevo objeto de búfer, se desperdicia mucho tiempo de procesador asignando y liberando memoria. En aplicaciones dependientes del tiempo, como reproductores multimedia, esta sobrecarga puede ser muy perjudicial para el rendimiento.

Para mitigar los problemas de rendimiento de las muestras asignadas por el lector, tanto el lector como el lector sincrónico admiten ejemplos asignados por el usuario. Para usar ejemplos asignados por la aplicación, el objeto de lectura realiza llamadas a un método de devolución de llamada de asignación de ejemplo que se implementa. La lógica usada por la devolución de llamada para enviar búferes al objeto de lectura es totalmente suya. Puede usar un grupo de búferes para todo el archivo o usar varios grupos de búferes, uno para cada salida o flujo, o cualquier otro esquema que funcione para la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Asignar búferes para la lectura de archivos**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Características de lectura de archivos**](file-reading-features.md)
</dt> </dl>

 

 




