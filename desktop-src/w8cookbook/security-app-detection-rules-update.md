---
title: Actualización de reglas de detección de aplicaciones de seguridad
description: Actualización de reglas de detección de aplicaciones de seguridad
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078501"
---
# <a name="security-app-detection-rules-update"></a>Actualización de reglas de detección de aplicaciones de seguridad

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


### <a name="description"></a>Descripción

Todas las aplicaciones de la tienda Windows que se agregan en Windows 8 se instalan en una ubicación común en "archivos de programa" (% ProgramFiles%) se denomina \\ archivos de programa \\ WindowsApps.

### <a name="manifestation"></a>Manifestación

Esto puede producir colisiones con las configuraciones existentes y algunos detectores antivirus/antimalware ven esta ubicación como una posible ubicación que es una causa de preocupación.

### <a name="mitigation"></a>Mitigación

Las recomendaciones actuales son:

-   Salir de \\ archivos de programa \\ WindowsApps para almacenar cualquier aplicación personalizada
-   Los proveedores de antivirus o antimalware deben actualizar su heurística para que no identifiquen esa ubicación como una ubicación de malware.

 

 




