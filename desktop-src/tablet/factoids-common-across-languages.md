---
description: Una serie de factoids describen la entrada que es común a todos los reconocedores de idioma y no necesitan tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los factoids que son comunes en todos los lenguajes.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids Common Across Languages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407a82c72367d0123414f72b083b1d3416cfc958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360010"
---
# <a name="factoids-common-across-languages"></a>Factoids Common Across Languages

Una serie de factoids describen la entrada que es común a todos los reconocedores de idioma y no necesitan tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los factoids que son comunes en todos los lenguajes.




| Factoid | Definición | Ejemplos | 
|---------|------------|----------|
| <strong>Dígitos</strong> | Establece el sesgo de un solo dígito. El reconocedor está sesgado hacia la devolución de solo dígitos cuando se establece este factoid.<br /> | 0-9<br /> | 
| <strong>Correo electrónico</strong> | Establece el sesgo de una dirección de correo electrónico.<br /> | someone@example.com<br /> | 
| <strong>Web</strong> | Establece el sesgo para varios formatos de dirección URL.<br /><blockquote>[!Note]<br />La configuración predeterminada del reconocedor incluye el <strong>factoid web.</strong> Por este problema, es posible que no observe una gran diferencia entre el factoid <strong>web</strong> y la configuración predeterminada. Sin embargo, el <strong>factoid web</strong> ayuda a eliminar los espacios entre las palabras de una dirección URL.</blockquote><br /> | http: \\ microsoft.net<br /> https://microsoft.us/<br /> https: \\ www.microsoft.au \<br />https://microsoft.com<br /> www.microsoft_world.com<br /> www.microsoft.us \<br /> http: \\www.microsoft.com\myfile.htm<br /> http: \\www.microsoft.com\myfile.html<br /> http: \\ www.microsoft.com\myfile.asp<br /> http: \\ www.microsoft.uk<br /> http: \\ www.microsoft.info<br /> www.microsoft.biz<br /> | 
| <strong>Valor predeterminado</strong> | Devuelve el reconocedor a su configuración predeterminada.<br /> | La configuración predeterminada de factoids para idiomas del oeste incluye el diccionario del sistema, el diccionario de usuarios, varias puntuaciones y los factoids <strong>Web</strong> y <strong>Number.</strong><br /> La configuración predeterminada de factoids para idiomas de Asia Oriental incluye todos los caracteres admitidos por el reconocedor.<br /> | 
| <strong>Ninguna</strong> | Deshabilita todos los factoids, diccionarios y el modelo de lenguaje.<br /> | Este factoid solo debe usarse si no desea que el reconocedor use reglas de gramática o diccionarios, incluido el diccionario del sistema. Este factoid es útil para la entrada de cadenas aleatorias, como códigos de producto. No use la marca Coerce con este factoid.<br /> | 




 

 

 




