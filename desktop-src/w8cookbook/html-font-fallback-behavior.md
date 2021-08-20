---
title: Comportamiento de reserva de fuentes HTML
description: Comportamiento de reserva de fuentes HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eabc2c009657adc9b77775c550244c4bbe6a5a3b8b262c8ce915cab4f9e5756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672053"
---
# <a name="html-font-fallback-behavior"></a>Comportamiento de reserva de fuentes HTML

## <a name="platform"></a>Plataforma

Clientes -** Windows 8.1  
**Servidores:** Windows Server 2012 R2  


## <a name="description"></a>Descripción

Microsoft está actualizando la lógica de las fuentes de interfaz de usuario para varios idiomas en Windows Store mediante HTML. En lugar de usar una sola fuente para todos los idiomas, la fuente de la interfaz de usuario ahora se determinará por idioma. Por ejemplo, las fuentes de interfaz de usuario para japonés ahora serán meiryo UI en aplicaciones que usan HTML.

## <a name="manifestation"></a>Manifestación

Las aplicaciones que dependían de una fuente antigua pueden tener un aspecto diferente; Aunque la apariencia de la aplicación se mejorará en general gracias a fuentes más legibles, podría haber un problema con los diseños que dependen de tamaños de contenido perfectos para píxeles. Por ejemplo, algunas líneas de contenido pueden ser más grandes que antes, lo que provoca saltos de línea inesperados o el redimensionamiento de los elementos del contenedor. Sin embargo, en la práctica no hemos detectado ningún problema con ninguna aplicación existente.

## <a name="solution"></a>Solución

Las aplicaciones afectadas pueden mitigar este comportamiento especificando una fuente determinada a través de CSS (por ejemplo, "font-family: Meiryo UI") en lugar de depender de las fuentes predeterminadas antiguas. En la tabla siguiente se proporciona la fuente de interfaz de usuario para cada uno de los nombres de script.



| Nombre del script        | Fuente de la interfaz de usuario               |
|--------------------|-----------------------|
| Árabe             | Segoe UI              |
| Armenio           | Segoe UI              |
| Bengalí            | Nirmala UI            |
| Bopomofo           | Microsoft JhengHei UI |
| Braille            | Segoe UI Symbol       |
| Buginés           | Leelawadee UI         |
| Sílabas canadienses | Gadugi                |
| Cheroqui           | Gadugi                |
| Copto             | Segoe UI Symbol       |
| Han (simplificado)   | Microsoft YaHei UI    |
| Han (tradicional)  | Microsoft JhengHei UI |
| Cirílico           | Segoe UI              |
| Devanagari         | Nirmala UI            |
| Deseret            | Segoe UI Symbol       |
| Etíope           | Ebrima                |
| Georgiano           | Segoe UI              |
| Glagolitic         | Segoe UI Symbol       |
| Gótico             | Segoe UI Symbol       |
| Griego              | Segoe UI              |
| Gujarati           | Nirmala UI            |
| Gurmukhi           | Nirmala UI            |
| Hebreo             | Segoe UI              |
| Cursiva anterior         | Segoe UI Symbol       |
| Javanés           | Texto javanés         |
| Japonés           | Interfaz de usuario de Meiryo             |
| Canarés            | Interfaz de usuario de Mirmala            |
| Jemer              | Leelawadee UI         |
| Coreano             | Malgun Gothic         |
| Lao                | Leelawadee            |
| Latín              | Segoe UI              |
| Malayalam          | Nirmala UI            |
| Mongol          | Mongolian Baiti       |
| Myanmar            | Myanmar Text          |
| N'Ko               | Ebrima                |
| Ogham              | Segoe UI Symbol       |
| Ol Chiki           | Nirmala UI            |
| Old Islandic         | Segoe UI Symbol       |
| Odia              | Nirmala UI            |
| Osmanya            | Ebrima                |
| Phags-pa           | Microsoft PhagsPa     |
| Rúnico              | Segoe UI Symbol       |
| Sora Sompeng       | Nirmala UI            |
| Cingalés            | Nirmala UI            |
| Siríaco             | Estrangelo Edessa     |
| Tai Le             | Microsoft Tai Le      |
| Nuevo Tai Lue        | Microsoft New Tai Lue |
| Tamil              | Nirmala UI            |
| Telugu             | Nirmala UI            |
| Tifinagh           | Ebrima                |
| Thaana             | MV Boli               |
| Tailandés               | Leelawadee UI         |
| Tibetano            | Microsoft Himalaya    |
| Vai                | Ebrima                |
| Yi                 | Microsoft Yi Baiti    |



 

 

 




