---
description: Los campos de campos de la página de códigos se usan en las estructuras FONTSIGNATURE y LOCALESIGNATURE. Tenga en cuenta que todas las configuraciones regionales no admiten páginas de códigos.
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: Campos de códigos de páginas de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f9df44ac14d935a026a10ab1e71eb7378840de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670010"
---
# <a name="code-page-bitfields"></a>Campos de códigos de páginas de códigos

Los campos de campos de la página de códigos se usan en las estructuras [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) y [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .

> [!Note]  
> Todas las configuraciones regionales no admiten páginas de códigos. Los campos de campos que se describen en este tema no se aplican a las configuraciones regionales Unicode. Para determinar los scripts admitidos para una configuración regional, la aplicación puede usar la configuración regional del identificador de configuración regional [ \_ SSCRIPTS](locale-sscripts.md) con [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex).

 

> [!Note]  
> La presencia de un bit en un campo de bits de una página de códigos no implica necesariamente que todas las cadenas de una configuración regional se puedan codificar en esa página de códigos sin pérdida. Para conservar los datos sin pérdida, se recomienda el uso de Unicode UTF-8 o UTF-16.

 



| bit          | Página de códigos | Descripción                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | Latin 1                                               |
| 1            | 1250      | Latín 2: Europa central                               |
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
| 19           | 949       | Código hangul en Coreano unificado (código TongHabHyung hangul) |
| 20           | 950       | Chino tradicional (Taiwán; RAE de Hong Kong, PRC)      |
| 21           | 1361      | Coreano (Johab)                                        |
| 22 - 29      |           | Reservado para ANSI alternativo y OEM                   |
| 30 - 31      |           | Reservado por el sistema.                                   |
| OEM          |           |                                                       |
| 32-46      |           | Reservado para OEM                                      |
| 47           | 1258      | Vietnamita                                            |
| 48           | 869       | Griego moderno                                          |
| 49           | 866       | Ruso                                               |
| 50           | 865       | Guantes                                                |
| 51           | 864       | Árabe                                                |
| 52           | 863       | Francés canadiense                                       |
| 53           | 862       |                                                       |
| 54           | 861       | Islandés                                             |
| 55           | 860       | Portugués                                            |
| 56           | 857       | Turco                                               |
| 57           | 855       | Cirílica principalmente Ruso                           |
| 58           | 852       | Latín 2                                               |
| 59           | 775       | Báltico                                                |
| 60           | 737       | Caracteres anteriormente 437G                                  |
| 61           | 708; 720  | Vietnamita ASMO 708                                      |
| 62           | 850       | Latín multilingüe 1                                  |
| 63           | 437       | US                                                    |



 

 

 



