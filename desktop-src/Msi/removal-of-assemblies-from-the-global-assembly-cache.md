---
description: El Windows de aplicaciones determina si se permite la eliminación de un ensamblado de Common Language Runtime basado en una lista de cliente que mantiene independientemente del ensamblado.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Eliminación de ensamblados de la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069656"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Eliminación de ensamblados de la caché global de ensamblados

El Windows de aplicaciones determina si se permite la eliminación de un ensamblado de Common Language Runtime basado en una lista de cliente que mantiene independientemente del ensamblado. El Windows mantiene un bit anclado para representar Windows Installer del ensamblado. El instalador ancla el ensamblado para el primer cliente Windows Installer y lo desanclar cuando se quita el último Windows installer. El ensamblado mantiene un bit de anclado para cada cliente de un ensamblado.

El Windows instalador no es directamente responsable de la eliminación física de ensamblados de Common Language Runtime del equipo. El instalador desanclará el ensamblado cuando se quite Windows cliente del instalador. Si el Windows es el último cliente del ensamblado, Common Language Runtime proporciona la opción de forzar una limpieza sincrónica del ensamblado. El proceso de limpieza es atómico y no hay ninguna disposición para una "reversión" en este momento. Todas las anulaciones de los ensamblados de Common Language Runtime deben producirse después de que el usuario haya tenido la oportunidad de cancelar la instalación o eliminación.

 

 



