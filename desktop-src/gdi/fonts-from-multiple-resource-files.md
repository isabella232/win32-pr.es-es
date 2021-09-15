---
description: Fuentes de varios archivos de recursos
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Fuentes de varios archivos de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570697"
---
# <a name="fonts-from-multiple-resource-files"></a>Fuentes de varios archivos de recursos

Normalmente, una fuente se encuentra en un único archivo de recursos de fuente. Sin embargo, la información de algunas fuentes se distribuye entre varios archivos. Por ejemplo, el tipo 1 de varias fuentes maestras requiere dos archivos:

-   .pfm para las métricas de fuente
-   .pfb para los bits de fuente

Para agregar una fuente de varios archivos al sistema, use las [**funciones AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx.**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) El *parámetro lpszFilename* de estas funciones debe apuntar a una cadena que contenga los nombres de archivo separados por la barra vertical o la canalización ( \| ). Por ejemplo, para especificar abcxxxxx.pfm y abcxxxxx.pfb para una fuente de tipo 1, use la cadena "abcxxxxx.pfm \| abcxxxxx.pfb".

[**AddFontResourceEx difiere**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) en que la aplicación que llama a **AddFontResourceEx** puede especificar la fuente como privada para sí misma o no enumerable.

Para agregar una fuente a partir de una imagen de memoria, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex). Esto permite que una aplicación use una fuente incrustada en un documento o una página web.

Para quitar una fuente que provenía de varios archivos de recursos, llame a [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) o [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), en función de la función utilizada para agregar la fuente. Debe especificar las mismas marcas que se usaron para agregar la fuente. Para quitar una fuente que se agregó de una imagen de memoria, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).

El uso de una fuente que procede de varios archivos de recursos de fuente es idéntico al uso de una fuente de un único archivo de recursos.

 

 
