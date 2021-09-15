---
description: Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003 que es responsable de mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Información general de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566357"
---
# <a name="overview-of-gdi"></a>Información general de GDI+

Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003 que es responsable de mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.

Como su nombre sugiere, GDI+ es el sucesor de Windows Interfaz de dispositivo gráfico (GDI), la interfaz del dispositivo gráfico incluida con versiones anteriores de Windows. Windows XP o Windows Server 2003 admite GDI para la compatibilidad con las aplicaciones existentes, pero los programadores de nuevas aplicaciones deben usar GDI+ para todas sus necesidades de gráficos porque GDI+ optimiza muchas de las funcionalidades de GDI y también proporciona características adicionales.

Una interfaz de dispositivo gráfico, como GDI+, permite a los programadores de aplicaciones mostrar información en una pantalla o impresora sin tener que preocuparse por los detalles de un dispositivo de pantalla determinado. El programador de aplicaciones realiza llamadas a los métodos proporcionados por GDI+ y esos métodos, a su vez, hacen las llamadas adecuadas a controladores de dispositivo específicos. GDI+ aísla la aplicación del hardware gráfico y es este aislamiento lo que permite a los desarrolladores crear aplicaciones independientes del dispositivo.

 

 



