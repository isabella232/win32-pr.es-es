---
title: Acerca de Windows Networking
description: Las aplicaciones pueden usar las funciones de WNet para agregar y cancelar conexiones de red y para recuperar información sobre la configuración actual de la red.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows WNet de red, descrito
- WNet WNet , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae26c503456d803edaed0b976e33020565aaa2364e7fc465c17a62cadf9068c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760485"
---
# <a name="about-windows-networking"></a>Acerca de Windows Networking

Las aplicaciones pueden usar las funciones de WNet para agregar y cancelar conexiones de red y para recuperar información sobre la configuración actual de la red.

En la ilustración siguiente se muestra la estructura de una red típica.

![estructura de red típica](images/csnet-01.png)

En la ilustración anterior, la jerarquía de los recursos Windows NT Server/Windows 2000 Server se proporciona en detalle como Proveedor de red \# 1. Los recursos de red de otros proveedores tienen sistemas jerárquicos diferentes. Una aplicación no necesita información sobre la jerarquía antes de empezar a trabajar con una red. Puede continuar desde la raíz de red (es decir, el recurso de contenedor más alto) y recuperar información sobre los recursos de la red a medida que se requiere la información.

Los recursos de red que contienen otros recursos se denominan *contenedores*. Los recursos de contenedor se encuentran en cuadros de la ilustración anterior.

Los recursos que no contienen otros recursos se denominan *objetos*. En la ilustración anterior, Sharepoint \# 1 y Sharepoint \# 2 son objetos . Un *sharepoint es* un objeto al que se puede acceder a través de la red. Entre los ejemplos de puntos de share se incluyen impresoras y directorios compartidos.

 

 




