---
description: El Windows Installer determina si se permite la eliminación de un ensamblado Common Language Runtime basado en una lista de clientes que se mantiene independientemente del ensamblado.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Eliminación de ensamblados de la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276839"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Eliminación de ensamblados de la caché global de ensamblados

El Windows Installer determina si se permite la eliminación de un ensamblado Common Language Runtime basado en una lista de clientes que se mantiene independientemente del ensamblado. El Windows Installer mantiene un bit de anclaje para representar a los clientes de Windows Installer del ensamblado. El instalador ancla el ensamblado para el primer Windows Installer cliente y lo desancla cuando se quita el último cliente de Windows Installer. El ensamblado mantiene un bit de anclaje por cada cliente de un ensamblado.

El Windows Installer no es responsable directamente de la eliminación física de los ensamblados de Common Language Runtime del equipo. El instalador desancla el ensamblado cuando se quita el último Windows Installer cliente. Si el Windows Installer es el último cliente del ensamblado, el Common Language Runtime proporciona la opción de forzar una limpieza sincrónica del ensamblado. El proceso de limpieza es atómico y no hay ningún aprovisionamiento para una "reversión" en este momento. Todo desanclaje de ensamblados de Common Language Runtime debe producirse después de que el usuario haya tenido la oportunidad de cancelar la instalación o la eliminación.

 

 



