---
title: Directrices de hardware de periféricos
description: Si su dispositivo de hardware no está diseñado para funcionar a través de una sesión remota, los proveedores deben asegurarse de que el software de controlador de dispositivo fuerce la deshabilitación de la redirección del dispositivo mediante una directiva del sistema o una directiva de grupo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418942"
---
# <a name="peripheral-hardware-guidelines"></a>Directrices de hardware de periféricos

En un cliente Conexión a Escritorio remoto (RDC), el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto) es el equipo local. Por lo tanto, los dispositivos como las unidades de disco y las impresoras conectadas al servidor aparecen como dispositivos locales para un cliente. Por el contrario, las unidades e impresoras conectadas a un terminal cliente pueden parecer dispositivos remotos, dependiendo de las opciones seleccionadas para la conexión, el servidor utilizado y la versión del software cliente que se utiliza.

Aunque la versión inicial de Servicios de Escritorio remoto no admitía las aplicaciones que envían la salida directamente a los puertos serie, paralelos y de sonido conectados al terminal del cliente, las versiones actuales permiten que estos dispositivos aparezcan como dispositivos locales en las aplicaciones que se ejecutan en la sesión Servicios de Escritorio remoto.

Si su dispositivo de hardware no está diseñado para funcionar a través de una sesión remota, los proveedores deben asegurarse de que el software de controlador de dispositivo fuerce la deshabilitación de la redirección del dispositivo mediante una directiva del sistema o una directiva de grupo.

 

 




