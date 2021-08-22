---
description: Cada Windows del instalador usa uno o varios componentes Windows instalador, y las características pueden compartir componentes.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Especificar relaciones Feature-Component datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1d7a79e35822d5a0ad67f43297ec461eb3c2fd766c946cc414a571c148de5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627875"
---
# <a name="specifying-feature-component-relationships"></a>Especificar relaciones Feature-Component datos

Cada [Windows del instalador usa](windows-installer-features.md) uno o varios componentes Windows [instalador,](windows-installer-components.md)y las características pueden compartir componentes. La [tabla FeatureComponents define](featurecomponents-table.md) la relación entre las características y los componentes. Consulte el [grupo de tablas principales y](core-tables-group.md) componentes y características [en](components-and-features.md) la información general Windows instalador. En esta sección agregará información a la tabla FeatureComponents del ejemplo Bloc de notas datos.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla FeatureComponents vacía.

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Béisbol  | Béisbol    |
| Concierto   | Concierto     |
| Baile     | Baile       |
| Fútbol  | Fútbol    |
| Ayuda      | Ayuda        |
| January   | January     |
| NewYears  | NewYears    |
| Bloc de notas   | Bloc de notas     |
| Léame    | Bloc de notas     |



 

[Continuar](adding-registry-information.md)

 

 



