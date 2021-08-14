---
description: El Windows de aplicaciones determina si se permite la eliminación de un ensamblado de Common Language Runtime basado en una lista de cliente que mantiene independientemente del ensamblado.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Eliminación de ensamblados de la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490142c1d3bd375b79513685198571b0638fbe16e03b99b39f59ec5ec9a9219
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327555"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Eliminación de ensamblados de la caché global de ensamblados

El Windows de aplicaciones determina si se permite la eliminación de un ensamblado de Common Language Runtime basado en una lista de cliente que mantiene independientemente del ensamblado. El Windows mantiene un bit de anclado para representar Windows installer del ensamblado. El instalador ancla el ensamblado para el primer cliente Windows Installer y lo desanclar cuando se quita el último Windows installer. El ensamblado mantiene un bit de anclado para cada cliente de un ensamblado.

El Windows instalador no es directamente responsable de la eliminación física de ensamblados de Common Language Runtime del equipo. El instalador desanclará el ensamblado cuando se Windows cliente del instalador. Si el Windows es el último cliente del ensamblado, Common Language Runtime proporciona la opción de forzar una limpieza sincrónica del ensamblado. El proceso de limpieza es atómico y no hay ninguna disposición para una "reversión" en este momento. Todas las anulaciones de los ensamblados de Common Language Runtime deben producirse después de que el usuario haya tenido la oportunidad de cancelar la instalación o eliminación.

 

 



