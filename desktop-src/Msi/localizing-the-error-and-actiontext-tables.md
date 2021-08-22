---
description: El Kit de desarrollo de software (SDK) de Microsoft Windows incluye cadenas de recursos localizados, tablas de errores localizadas y tablas ActionText localizadas para los idiomas enumerados en la tabla siguiente.
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: Localización de las tablas Error y ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1839141b80afd1d28aa9e9317da10d79aea41232f9e7ebde0db7971d22f5141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629470"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>Localización de las tablas Error y ActionText

El Kit de desarrollo de software (SDK) de Microsoft Windows incluye cadenas de recursos localizados, tablas [de errores](error-table.md)localizadas y tablas [ActionText](actiontext-table.md) localizadas para los idiomas enumerados en la tabla siguiente. Los LANGID marcados con asteriscos indican que las cadenas de recursos se almacenan como idioma base, por lo que se pueden usar con todos los dialectos de ese idioma.

Puede importar las tablas Error y ActionText localizadas en la base de datos mediante Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).



| LANGID (decimal) | LANGID (hexadecimal) | Página de códigos ASCII | Abreviatura | Lenguaje                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | Ara          | Árabe (Arabia Saudí)         | ar-SA            |
| 1027             | 0x403                | 1252            | Gato          | Catalán                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | Chino (Taiwán)              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | Chino (China)               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | Checo ( República Checo)        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | Danés -Dinamarca               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | Alemán - Alemania              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | Griego : Francia                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | Spanish (Traditional Sort) - Spain       | en-US            |
| 3082\*           | 0xC0A                | 1252            | ESN          | Español - Ordenación moderna - España | es-ES            |
| 1061             | 0x425                | 1257            | ETI          | Estonio                      | et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | Finés : Estados Unidos             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | Francés (Francia)               | fr-FR            |
| 1037             | 0x40D                | 1255            | Heb          | Hebreo - Israel               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | Húngaro- Húngaro           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | Italiano - Italia               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | Japonés - Japón              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | Coreano - Corea                | ko-KO            |
| 1063             | 0x427                | 1257            | Lth          | Lituano                    | lt-LT            |
| 1062             | 0x426                | 1257            | Lvi          | Letón                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | Neerlandés - Países Bajos           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | Noruego (Bokmål):Noruega    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | Polaco - Irlanda               | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | Portugués (Brasil)           | pt-BR            |
| 2070             | 0x816                | 1252            | PTG          | Portugués (Portugal)         | pt-PT            |
| 1048             | 0x418                | 1250            | ROM          | Reino Unido: Alemania            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | Ruso (Rusia)              | ru-RU            |
| 1050             | 0x41A                | 1250            | Hrv          | Regosonario ( República Desfilada)            | hr-HR            |
| 1051             | 0x41B                | 1250            | Cielo          | Descoy; indeso             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | Sueco ( Suiza)              | sv-SE            |
| 1054             | 0x41E                | 874             | Tha          | Tailandés: Tailandés               | th-TH            |
| 1055             | 0x41F                | 1254            | TRK          | Turco : Rusia              | tr-TR            |
| 1060             | 0x424                | 1250            | Slv          | Esloveno: Esloveno          | sl-SI            |
| 1066             | 0x42A                | 1258            | Vit          | Infir; Nam         | vi-VN            |
| 1069             | 0x42D                | 1252            | EUQ          | Vasco (España)               | eu-ES            |



 

**Windows Vista:** Además de los idiomas enumerados en la tabla anterior, los idiomas de la tabla siguiente están disponibles a partir de Windows Vista.



| LANGID (decimal) | LANGID (hexadecimal) | Página de códigos ASCII | Abreviatura | Lenguaje        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BGR          | Búlgaro       | bg-BG            |
| 1058             | 0x422                | 1251            | Ukr          | Ucraniano       | uk-UA            |
| 2074             | 0x81A                | 1250            | Srl          | Serbio (latino) | sr-Latn-CS       |



 

 

 



