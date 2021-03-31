---
description: Un monitor es una biblioteca de vínculos dinámicos (DLL) que examina las capturas en tiempo real del tráfico de red.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001230"
---
# <a name="monitors"></a>Monitores

Un monitor es una biblioteca de vínculos dinámicos (DLL) que examina las capturas en tiempo real del tráfico de red. Busca condiciones predefinidas y, después, genera eventos cuando se detectan esas condiciones. Por ejemplo, se puede desencadenar un evento cuando se intenta un salto de red, cuando una estación de trabajo no autorizada está entregando las direcciones IP o cuando se produce un error en un enrutador.

> [!Note]  
> Si necesita realizar análisis detallados de los datos de red que requieren un análisis posterior a la captura, debe usar aplicaciones de [*analizador*](p.md) y de [*expertos*](e.md) .

 

El [*servicio de control de supervisión*](m.md) (MCSVC) proporciona el marco de trabajo para administrar los monitores. Proporciona funciones para cargar los archivos DLL del monitor y una interfaz de comunicaciones con la herramienta de control de supervisión para que pueda crear, configurar, iniciar, detener y deshabilitar varias instancias de los monitores.

Los monitores se ejecutan en dos subprocesos de ejecución. MCSVC proporciona el primer subproceso, que proporciona control directo del monitor. El segundo subproceso lo proporciona el [*proveedor de paquetes de red*](n.md) (NPP), que proporciona una manera de pasar los datos capturados, las estadísticas y el estado de la captura del NPP de vuelta al monitor.

Puede haber más de una instancia del mismo monitor para cada interfaz NPP en tiempo de ejecución que se usa para capturar datos.

 

 



