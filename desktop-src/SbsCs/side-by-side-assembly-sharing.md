---
description: En la ilustración siguiente se muestra cómo dos aplicaciones pueden compartir un ensamblado mediante el método tradicional de uso compartido de ensamblados.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Uso compartido de ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002765"
---
# <a name="side-by-side-assembly-sharing"></a>Uso compartido de ensamblados en paralelo

En la ilustración siguiente se muestra cómo dos aplicaciones pueden compartir un ensamblado mediante el método tradicional de uso compartido de ensamblados. Un problema con el uso compartido de ensamblados tradicional se produce cuando una aplicación instala una versión de un ensamblado, normalmente un archivo DLL, que no es compatible con versiones anteriores. La aplicación que acaba de instalar funciona, pero es posible que las aplicaciones que dependen de la versión anterior del archivo DLL dejen de funcionar.

![representación de dos aplicaciones que comparten un ensamblado](images/sxs1.png)

La solución de ensamblados en paralelo y aplicación aislada permite que las distintas versiones del mismo ensamblado Win32 se ejecuten al mismo tiempo en el mismo sistema sin conflictos. Al especificar la versión de ensamblado en paralelo que debe usar la aplicación, los desarrolladores pueden garantizar que la configuración que prueba se duplicará siempre en el equipo del usuario. El uso compartido simultáneo se muestra en la ilustración siguiente.

![implementación de uso compartido de ensamblados en paralelo](images/sxs2.png)

Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](about-isolated-applications-and-side-by-side-assemblies.md).

 

 



