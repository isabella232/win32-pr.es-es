---
description: Los dos modos de asignación definidos por la aplicación (MM \_ anisotrópico y mm \_ ) se proporcionan para los modos de asignación específicos de la aplicación.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modos de asignación de Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997436"
---
# <a name="application-defined-mapping-modes"></a>Modos de asignación de Application-Defined

Los dos modos de asignación definidos por la aplicación (MM \_ anisotrópico y mm \_ ) se proporcionan para los modos de asignación específicos de la aplicación. El \_ modo anisotrópico de mm garantiza que las unidades lógicas en la dirección x y en la dirección y son iguales, mientras que el \_ modo ANISOTRÓPICO de mm permite que las unidades difieran. Una aplicación de CAD o de dibujo puede beneficiarse del modo de asignación de anisotrópico de MM \_ , pero puede que sea necesario especificar unidades lógicas que se correspondan con los incrementos de la escala de un ingeniero (1/64 de pulgada). Estas unidades serían difíciles de obtener con los modos de asignación predefinidos (MM \_ HIENGLISH o mm \_ HIMETRIC); sin embargo, se pueden obtener fácilmente seleccionando el \_ modo anisotrópico de MM (o x \_ ). En el ejemplo siguiente se muestra cómo establecer unidades lógicas en 1/64 pulgadas:


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



