---
description: Los campos de bits de la página de códigos se usan en las estructuras FONTSIGNATURE y LOCALIGNATURE. Nota Todas las configuraciones regionales no admiten páginas de códigos.
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: Campos de bits de página de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfd16bb04f88201b571759cd09eb9d3e99ef43eb7c7b1c1c40c93e246833aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898761"
---
# <a name="code-page-bitfields"></a>Campos de bits de página de códigos

Los campos de bits de la página de códigos se usan en las estructuras [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) [**y LOCALIGNATURE.**](/windows/win32/api/wingdi/ns-wingdi-localesignature)

> [!Note]  
> Todas las configuraciones regionales no admiten páginas de códigos. Los campos de bits descritos en este tema no se aplican a las configuraciones regionales Unicode. Para determinar los scripts admitidos para una configuración regional, la aplicación puede usar la constante de identificador de configuración regional [LOCALE \_ SSCRIPTS](locale-sscripts.md) con [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex).

 

> [!Note]  
> La presencia de un bit en un campo de bits de página de códigos no significa necesariamente que todas las cadenas de una configuración regional se puedan codificar en esa página de códigos sin pérdida. Para conservar los datos sin pérdida, se recomienda usar Unicode UTF-8 o UTF-16.

 



| bit          | Página de códigos | Descripción                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | Latin 1                                               |
| 1            | 1250      | Latino 2: Centro de Europa                               |
| 2            | 1251      | Cirílico                                              |
| 3            | 1253      | Griego                                                 |
| 4            | 1254      | Turco                                               |
| 5            | 1255      | Hebreo                                                |
| 6            | 1256      | Árabe                                                |
| 7            | 1257      | Báltico                                                |
| 8            | 1258      | Vietnamita                                            |
| 9 - 15       |           | Reservado para ANSI                                     |
| ANSI y OEM |           |                                                       |
| 16           | 874       | Tailandés                                                  |
| 17           | 932       | Japonés, Shift-JIS                                   |
| 18           | 936       | Chino simplificado (PRC, Singapur)                   |
| 19           | 949       | Código Hangul unificado coreano (código Hangul TongHabHyung) |
| 20           | 950       | Chino tradicional (Taiwán; RAE de Hong Kong, PRC)      |
| 21           | 1361      | Coreano (Johab)                                        |
| 22 - 29      |           | Reservado para ANSI y OEM alternativos                   |
| 30 - 31      |           | Reservado por sistema.                                   |
| OEM          |           |                                                       |
| 32 - 46      |           | Reservado para OEM                                      |
| 47           | 1258      | Vietnamita                                            |
| 48           | 869       | Griego moderno                                          |
| 49           | 866       | Ruso                                               |
| 50           | 865       | Nórdico                                                |
| 51           | 864       | Árabe                                                |
| 52           | 863       | Francés canadiense                                       |
| 53           | 862       |                                                       |
| 54           | 861       | Islandés                                             |
| 55           | 860       | Portugués                                            |
| 56           | 857       | Turco                                               |
| 57           | 855       | Cirílico; principalmente ruso                           |
| 58           | 852       | Latin 2                                               |
| 59           | 775       | Báltico                                                |
| 60           | 737       | Griego; anteriormente 437G                                  |
| 61           | 708; 720  | Árabe; ASMO 708                                      |
| 62           | 850       | Idioma latino multilingüe 1                                  |
| 63           | 437       | US                                                    |



 

 

 



