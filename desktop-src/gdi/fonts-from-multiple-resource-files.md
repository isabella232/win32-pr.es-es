---
description: Fuentes de varios archivos de recursos
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Fuentes de varios archivos de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/17/2021
ms.locfileid: "104998875"
---
# <a name="fonts-from-multiple-resource-files"></a>Fuentes de varios archivos de recursos

Normalmente, una fuente se encuentra en un archivo de recursos de fuente único. Sin embargo, la información de algunas fuentes se distribuye entre varios archivos. Por ejemplo, escriba 1 varias fuentes maestras requieren dos archivos:

-   . PFM para las métricas de fuente
-   . PFB para los bits de fuente

Para agregar una fuente de varios archivos al sistema, use las funciones [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) . El parámetro *lpszFilename* de estas funciones debe apuntar a una cadena que contenga los nombres de archivo separados por la barra vertical o la canalización ( \| ). Por ejemplo, para especificar abcxxxxx. PFM y abcxxxxx. PFB para una fuente de tipo 1, use la cadena "abcxxxxx. PFM \| abcxxxxx. PFB".

[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) difiere de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) en que la aplicación que llama a **AddFontResourceEx** puede especificar la fuente como privada para sí misma o no Enumerable.

Para agregar una fuente de una imagen de memoria, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex). Esto permite que una aplicación use una fuente que está incrustada en un documento o una página web.

Para quitar una fuente que proviene de varios archivos de recursos, llame a [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) o [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), en función de la función utilizada para agregar la fuente. Debe especificar las mismas marcas que se usaron para agregar la fuente. Para quitar una fuente que se ha agregado a partir de una imagen de memoria, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).

El uso de una fuente que proviene de varios archivos de recursos de fuente es idéntico al uso de una fuente de un archivo de recursos único.

 

 
