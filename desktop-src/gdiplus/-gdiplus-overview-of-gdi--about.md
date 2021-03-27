---
description: Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003, que es responsable de Mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Información general sobre GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997461"
---
# <a name="overview-of-gdi"></a>Información general sobre GDI+

Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003, que es responsable de Mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.

Como su nombre sugiere, GDI+ es el sucesor de Windows Interfaz de dispositivo gráfico (GDI), la interfaz de dispositivo gráfico incluida en versiones anteriores de Windows. Windows XP o Windows Server 2003 admiten GDI para la compatibilidad con las aplicaciones existentes, pero los programadores de aplicaciones nuevas deben usar GDI+ para todas sus necesidades de gráficos porque GDI+ optimiza muchas de las capacidades de GDI y también proporciona características adicionales.

Una interfaz de dispositivo gráfico, como GDI+, permite a los programadores de aplicaciones Mostrar información en una pantalla o una impresora sin tener que preocuparse de los detalles de un determinado dispositivo de pantalla. El programador de la aplicación realiza llamadas a los métodos proporcionados por las clases de GDI+ y, a su vez, realiza las llamadas adecuadas a controladores de dispositivos específicos. GDI+ aísla la aplicación del hardware de gráficos y es este aislamiento que permite a los desarrolladores crear aplicaciones independientes del dispositivo.

 

 



