---
title: Comportamiento de reserva de fuente HTML
description: Comportamiento de reserva de fuente HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105705061"
---
# <a name="html-font-fallback-behavior"></a>Comportamiento de reserva de fuente HTML

## <a name="platform"></a>Plataforma

Clientes-* * Windows 8.1  
**Servidores:** Windows Server 2012 R2  


## <a name="description"></a>Descripción

Microsoft está actualizando la lógica de las fuentes de interfaz de usuario para varios idiomas en aplicaciones de la tienda Windows con HTML. En lugar de usar una sola fuente para todos los idiomas, la fuente de la interfaz de usuario se determinará en función de cada idioma. Por ejemplo, las fuentes de interfaz de usuario para japonés ahora serán la interfaz de usuario de Meiryo en aplicaciones que usan HTML.

## <a name="manifestation"></a>Manifestación

Las aplicaciones que dependen de una fuente antigua pueden tener un aspecto diferente. Aunque el aspecto de la aplicación se mejorará globalmente gracias a las fuentes más legibles, podría haber un problema con los diseños que dependen de tamaños de contenido con píxeles perfectos. Por ejemplo, algunas líneas de contenido pueden ser mayores de lo anterior, lo que provoca saltos de línea inesperados y/o el cambio de tamaño de los elementos del contenedor. Sin embargo, en la práctica no hemos observado ningún problema con las aplicaciones existentes.

## <a name="solution"></a>Solución

Las aplicaciones afectadas pueden mitigar este comportamiento mediante la especificación de una fuente determinada a través de CSS (por ejemplo, "font-family: Meiryo UI") en lugar de depender de las fuentes predeterminadas anteriores. En la tabla siguiente se proporciona la fuente de la interfaz de usuario para cada uno de los nombres de script.



| Nombre del script        | Fuente de la interfaz de usuario               |
|--------------------|-----------------------|
| Árabe             | Segoe UI              |
| Armenio           | Segoe UI              |
| Bengalí            | Nirmala UI            |
| Bopomofo           | Microsoft JhengHei UI |
| Pantallas            | Segoe UI Symbol       |
| Buginés           | Leelawadee UI         |
| Silábico canadiense | Gadugi                |
| Cheroqui           | Gadugi                |
| Copto             | Segoe UI Symbol       |
| Han (simplificado)   | Microsoft YaHei UI    |
| Han (tradicional)  | Microsoft JhengHei UI |
| Cirílico           | Segoe UI              |
| Devanagari         | Nirmala UI            |
| Deseret            | Segoe UI Symbol       |
| Dígito           | Ebrima                |
| Georgiano           | Segoe UI              |
| Letra         | Segoe UI Symbol       |
| Gótico             | Segoe UI Symbol       |
| Griego              | Segoe UI              |
| Gujarati           | Nirmala UI            |
| Gurmukhi           | Nirmala UI            |
| Hebreo             | Segoe UI              |
| Cursiva antigua         | Segoe UI Symbol       |
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
| OL Chiki           | Nirmala UI            |
| Turca anterior         | Segoe UI Symbol       |
| Odia              | Nirmala UI            |
| Osmanya            | Ebrima                |
| Phags-pa           | Microsoft PhagsPa     |
| Rúnica              | Segoe UI Symbol       |
| Sora Sompeng       | Nirmala UI            |
| Cingalés            | Nirmala UI            |
| Siríaco             | Estrangelo Edessa     |
| Tai le             | Microsoft Tai Le      |
| Nuevo tai lue moderno        | Microsoft New Tai Lue |
| Tamil              | Nirmala UI            |
| Telugu             | Nirmala UI            |
| Tifinagh           | Ebrima                |
| Thaana             | MV Boli               |
| Tailandés               | Leelawadee UI         |
| Tibetano            | Microsoft Himalaya    |
| Vai                | Ebrima                |
| Yi                 | Microsoft Yi Baiti    |



 

 

 




