---
description: Un monitor es una biblioteca de vínculos dinámicos (DLL) que examina las capturas en tiempo real del tráfico de red.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245337"
---
# <a name="monitors"></a>Monitores

Un monitor es una biblioteca de vínculos dinámicos (DLL) que examina las capturas en tiempo real del tráfico de red. Busca condiciones predefinidas y, a continuación, genera eventos cuando se detectan esas condiciones. Por ejemplo, se puede producir un evento cuando se intenta un salto de red, cuando una estación de trabajo no segura está entregando direcciones IP o cuando se produce un error en un enrutador.

> [!Note]  
> Si necesita realizar análisis detallados sobre los datos de red que requieren [](e.md) un análisis posterior a la captura, debe usar aplicaciones expertos [*y analizadores.*](p.md)

 

Monitor [*Control Service*](m.md) (MCSVC) proporciona el marco para administrar los monitores. Proporciona funciones para cargar los archivos DLL de supervisión y una interfaz de comunicaciones en la herramienta de control de supervisión para que pueda crear, configurar, iniciar, detener y deshabilitar varias instancias de los monitores.

Los monitores se ejecutan en dos subprocesos de ejecución. MCSVC proporciona el primer subproceso, que proporciona control directo del monitor. El segundo subproceso lo [](n.md) proporciona el proveedor de paquetes de red (NPP), que proporciona una manera de pasar los datos de red capturados, las estadísticas y el estado de la captura del NPP de vuelta al monitor.

Puede existir más de una instancia del mismo monitor para cada interfaz de NPP en tiempo de ejecución que se usa para capturar datos.

 

 



