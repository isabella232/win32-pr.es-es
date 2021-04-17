---
description: Cada Windows Installer característica usa uno o varios componentes Windows Installer, y las características pueden compartir componentes.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Especificar relaciones Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677432"
---
# <a name="specifying-feature-component-relationships"></a>Especificar relaciones Feature-Component

Cada [Windows Installer característica](windows-installer-features.md) usa uno o varios [componentes Windows Installer](windows-installer-components.md), y las características pueden compartir componentes. La [tabla FeatureComponents](featurecomponents-table.md) define la relación entre las características y los componentes de. Vea el [grupo de tablas principales](core-tables-group.md) y [los componentes y características](components-and-features.md) en la información general de Windows Installer. En esta sección, agregará información a la tabla FeatureComponents del ejemplo de Bloc de notas.

Use el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla FeatureComponents vacía.

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Baloncesto  | Baloncesto    |
| Concierto   | Concierto     |
| Dance     | Dance       |
| Balón  | Balón    |
| Ayuda      | Ayuda        |
| January   | January     |
| NewYears  | NewYears    |
| Bloc de notas   | Bloc de notas     |
| Léame    | Bloc de notas     |



 

[Continuar](adding-registry-information.md)

 

 



