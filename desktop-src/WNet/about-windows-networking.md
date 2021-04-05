---
title: Acerca de las redes de Windows
description: Las aplicaciones pueden usar las funciones de WNet para agregar y cancelar conexiones de red y para recuperar información acerca de la configuración actual de la red.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows Networking WNet, descrito
- WNet WNet, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076328"
---
# <a name="about-windows-networking"></a>Acerca de las redes de Windows

Las aplicaciones pueden usar las funciones de WNet para agregar y cancelar conexiones de red y para recuperar información acerca de la configuración actual de la red.

En la ilustración siguiente se muestra la estructura de una red típica.

![estructura de red típica](images/csnet-01.png)

En la ilustración anterior, la jerarquía de los recursos de Windows NT Server/Windows 2000 Server se proporciona en detalle como proveedor de red \# 1. Los recursos de red de otros proveedores tienen diferentes sistemas jerárquicos. Una aplicación no necesita información sobre la jerarquía antes de empezar a trabajar con una red. Puede continuar desde la raíz de red (es decir, el recurso de contenedor de nivel superior) y recuperar información acerca de los recursos de la red a medida que se requiere la información.

Los recursos de red que contienen otros recursos se denominan *contenedores*. Los recursos de contenedor se encuentran en los cuadros de la ilustración anterior.

Los recursos que no contienen otros recursos se denominan *objetos*. En la ilustración anterior, SharePoint \# 1 y SharePoint \# 2 son objetos. Un *SharePoint* es un objeto al que se puede tener acceso a través de la red. Entre los ejemplos de SharePoint se incluyen impresoras y directorios compartidos.

 

 




