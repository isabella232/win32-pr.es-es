---
title: Directrices de hardware periférico
description: Si su dispositivo de hardware no está diseñado para funcionar en una sesión remota, los proveedores deben asegurarse de que el software del controlador de dispositivo fuerza la deshabilitación del redireccionamiento del dispositivo mediante una directiva del sistema o una directiva de grupo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967996"
---
# <a name="peripheral-hardware-guidelines"></a>Directrices de hardware periférico

Para un Conexión a Escritorio remoto remoto (RDC), el servidor Escritorio remoto host de sesión de Escritorio remoto es el equipo local. Por lo tanto, los dispositivos como las unidades de disco y las impresoras conectadas al servidor aparecen como dispositivos locales para un cliente. Por el contrario, las unidades e impresoras conectadas a un terminal cliente pueden parecer dispositivos remotos, en función de las opciones seleccionadas para la conexión, el servidor usado y la versión del software cliente utilizado.

Aunque la versión inicial de Servicios de Escritorio remoto no admite aplicaciones que envían salidas directamente a puertos serie, paralelos y de sonido conectados al terminal cliente, las versiones actuales permiten que estos dispositivos aparezcan como dispositivos locales a las aplicaciones que se ejecutan en la sesión Servicios de Escritorio remoto.

Si su dispositivo de hardware no está diseñado para funcionar en una sesión remota, los proveedores deben asegurarse de que el software del controlador de dispositivo fuerza la deshabilitación del redireccionamiento del dispositivo mediante una directiva del sistema o una directiva de grupo.

 

 




