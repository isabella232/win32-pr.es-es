---
description: Al combinar un módulo en una base de datos de instalación, hay dos lenguajes importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Abrir un Multiple-Language combinar en un lenguaje específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251019"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Abrir un Multiple-Language combinar en un lenguaje específico

Al combinar un módulo en una base de datos de instalación, hay dos lenguajes importantes. El primero es el idioma del paquete de instalación de destino especificado por [**ProductLanguage**](productlanguage.md) en la [tabla de propiedades](property-table.md). El segundo es el idioma del módulo de combinación que aparece en la columna Idioma de [la tabla ModuleSignature](modulesignature-table.md).

La herramienta de combinación puede pasar el idioma del paquete de instalación al módulo cuando el paquete se abre para una combinación. Sin embargo, a veces puede ser necesario pasar por alto el idioma del destino y solicitar que el módulo se abra en otro idioma, por ejemplo, un paquete en inglés que instale los recursos en inglés y alemán desde el módulo.

Al abrir un módulo con una solicitud de idioma, la herramienta de combinación comprueba el idioma solicitado con los idiomas especificados en la columna Idioma de [la tabla ModuleSignature](modulesignature-table.md).

El siguiente proceso se usa para determinar qué lenguaje se va a usar.

**Para determinar qué idioma se va a usar**

1.  Si el idioma de [la tabla ModuleSignature es](modulesignature-table.md) igual o más general que el idioma solicitado, se abre el módulo.
2.  Si el módulo admite el idioma exacto solicitado, se usa ese idioma.
3.  Si el módulo admite el grupo de idiomas del idioma solicitado, por ejemplo, compruebe 9 si se solicitó 1033 pero no se encontró en el paso 2.
4.  Compruebe si hay una transformación de idioma que cambie el módulo a neutro.
5.  Si ninguno de los pasos anteriores se realiza correctamente, el módulo no admite el idioma solicitado y se produce un error en la combinación.

 

 



