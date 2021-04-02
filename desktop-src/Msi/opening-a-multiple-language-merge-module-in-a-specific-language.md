---
description: Al combinar un módulo en una base de datos de instalación, hay dos lenguajes importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Abrir un módulo de combinación de Multiple-Language en un idioma específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082258"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Abrir un módulo de combinación de Multiple-Language en un idioma específico

Al combinar un módulo en una base de datos de instalación, hay dos lenguajes importantes. El primero es el idioma del paquete de instalación de destino especificado por [**ProductLanguage**](productlanguage.md) en la [tabla de propiedades](property-table.md). El segundo es el idioma del módulo de combinación que aparece en la columna Language de la [tabla ModuleSignature](modulesignature-table.md).

El idioma del paquete de instalación se puede pasar al módulo mediante la herramienta de combinación cuando se abre el paquete para una combinación. Sin embargo, a veces puede ser necesario omitir el idioma del destino y solicitar que el módulo se abra en otro idioma, por ejemplo, un paquete en inglés que instale los recursos en inglés y en alemán desde el módulo.

Al abrir un módulo con una solicitud de lenguaje, la herramienta de combinación comprueba el idioma solicitado con los idiomas especificados en la columna idioma de la [tabla ModuleSignature](modulesignature-table.md).

El siguiente proceso se utiliza para determinar el idioma que se va a utilizar.

**Para determinar el idioma que se va a usar**

1.  Si el idioma de la [tabla ModuleSignature](modulesignature-table.md) es igual o más general que el idioma solicitado, se abre el módulo.
2.  Si el módulo admite el lenguaje exacto solicitado, se usa ese idioma.
3.  Si el módulo admite el grupo de idiomas del idioma solicitado, se usa el grupo de idioma; por ejemplo, Active 9 Si se solicitó 1033 pero no se encontró en el paso 2.
4.  Compruebe si hay una transformación de idioma que cambie el módulo a neutro.
5.  Si ninguno de los pasos anteriores se realiza correctamente, el módulo no admite el idioma solicitado y se produce un error en la combinación.

 

 



