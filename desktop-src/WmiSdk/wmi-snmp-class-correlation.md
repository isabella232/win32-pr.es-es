---
description: La correlación afecta al conjunto de clases devueltas desde SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlación de clases SNMP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276248"
---
# <a name="wmi-snmp-class-correlation"></a>Correlación de clases SNMP de WMI

La correlación afecta al conjunto de clases devueltas desde SMIR. Las clases correlacionadas son aquellas que se sabe que admite un dispositivo SNMP determinado en el momento en que se produce la enumeración. La enumeración no correlacionada devuelve todas las clases presentes en el SMIR, independientemente de si el dispositivo las admite. La correlación es una característica del proveedor SNMP de WMI y se puede desactivar o activar (valor predeterminado).

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

La correlación podría impedir ver todas las clases que realmente admite un dispositivo. Si sabe que se admite una clase determinada, pero no aparece en SMIR, esto podría deberse a varios motivos, uno de los cuales es una correlación. Considere la posibilidad de desactivar la correlación antes de escribir en el dispositivo en cuestión. Sin embargo, si se desactiva la correlación, se produce la probabilidad de que muchas clases no admitidas por el dispositivo aparezcan en SMIR. Además, existe un costo de rendimiento al usar la correlación porque el dispositivo se consulta para ver qué clases admite. Cuando se activa la correlación, el proveedor SNMP produce una enumeración de clases admitidas por el dispositivo similar al resultado de ejecutar una herramienta de *recorrido de MIB* .

Por ejemplo, un administrador de red desea conocer varias partes clave de los datos de todos los concentradores administrados en una red determinada. Ya existe una base de datos de los dispositivos actuales y sus MIB compatibles, por lo que no es necesario depender de la función de correlación del dispositivo para proporcionar los elementos de datos admitidos. En este caso, la correlación podría desactivarse.

En el ejemplo siguiente se muestra cómo desactivar la correlación.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



Por otro lado, es posible que otro administrador de red desee supervisar todas las unidades de disco de la máquina UNIX en la red, pero no está familiarizado con los datos de la MIB de esas máquinas. En ese caso, se activaría la correlación.

 

 



