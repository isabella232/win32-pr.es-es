---
title: Qué debe hacer la instalación
description: El OID debe hacer referencia a los nuevos atributos a los que se hace referencia en el paso 3 porque el nombre del nuevo atributo no está presente en la caché de esquema en este momento.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Qué debe hacer la instalación de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993883"
---
# <a name="what-the-installation-must-do"></a>Qué debe hacer la instalación

Las aplicaciones que extienden el esquema deben aplicar las actualizaciones tal y como se describe en el procedimiento siguiente.

**Para aplicar actualizaciones al extender el esquema**

1.  Agregue los nuevos atributos.
2.  Agregue las nuevas clases.
3.  Agregue los nuevos atributos a las clases.
4.  Desencadenar una recarga de caché.

El OID debe hacer referencia a los nuevos atributos a los que se hace referencia en el paso 3 porque el nombre del nuevo atributo no está presente en la caché de esquema en este momento.

El paso 4 no es necesario si las extensiones no se van a usar inmediatamente; las extensiones aparecerán en la caché de esquema en unos 5 minutos, en función de la carga del sistema. Para obtener más información acerca de la caché de esquema y cómo desencadenar una recarga de caché, vea [actualizar la caché de esquema](updating-the-schema-cache.md).

 

 




