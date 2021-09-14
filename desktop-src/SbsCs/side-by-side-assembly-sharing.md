---
description: En la ilustración siguiente se muestra cómo dos aplicaciones pueden compartir un ensamblado mediante el método tradicional de uso compartido de ensamblados.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Uso compartido de ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073805"
---
# <a name="side-by-side-assembly-sharing"></a>Uso compartido de ensamblados en paralelo

En la ilustración siguiente se muestra cómo dos aplicaciones pueden compartir un ensamblado mediante el método tradicional de uso compartido de ensamblados. Un problema con el uso compartido tradicional de ensamblados se produce cuando una aplicación instala una versión de un ensamblado (normalmente un archivo DLL) que no es compatible con versiones anteriores. La aplicación que acaba de instalar funciona, pero es posible que las aplicaciones que dependían de la versión anterior del archivo DLL ya no funcionen.

![representación de dos aplicaciones que comparten un ensamblado](images/sxs1.png)

La aplicación aislada y la solución de ensamblado en paralelo permiten que distintas versiones del mismo ensamblado Win32 se ejecuten al mismo tiempo en el mismo sistema sin conflictos. Al especificar qué versión de ensamblado en paralelo debe usar la aplicación, los desarrolladores pueden garantizar que la configuración que pruebe siempre se duplicará en el equipo del usuario. El uso compartido en paralelo se muestra en la ilustración siguiente.

![implementación del uso compartido de ensamblados en paralelo](images/sxs2.png)

Para obtener más información, vea [Acerca de las aplicaciones aisladas y ensamblados en paralelo.](about-isolated-applications-and-side-by-side-assemblies.md)

 

 



