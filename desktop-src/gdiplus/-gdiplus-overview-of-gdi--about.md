---
description: Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003 que es responsable de mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Información general de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ca4eadf9eaf27cbe35103753a49c4bc25d2974ee1051481b0b52787a6602e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830765"
---
# <a name="overview-of-gdi"></a>Información general de GDI+

Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003 que es responsable de mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.

Como su nombre sugiere, GDI+ es el sucesor de Windows Interfaz de dispositivo gráfico (GDI), la interfaz del dispositivo gráfico incluida con versiones anteriores de Windows. Windows XP o Windows Server 2003 admite GDI para la compatibilidad con aplicaciones existentes, pero los programadores de nuevas aplicaciones deben usar GDI+ para todas sus necesidades de gráficos porque GDI+ optimiza muchas de las funcionalidades de GDI y también proporciona características adicionales.

Una interfaz de dispositivo gráfico, como GDI+, permite a los programadores de aplicaciones mostrar información en una pantalla o impresora sin tener que preocuparse por los detalles de un dispositivo de pantalla determinado. El programador de aplicaciones realiza llamadas a los métodos proporcionados por GDI+ y esos métodos, a su vez, hacen las llamadas adecuadas a controladores de dispositivo específicos. GDI+ aísla la aplicación del hardware gráfico y es este aislamiento lo que permite a los desarrolladores crear aplicaciones independientes del dispositivo.

 

 



