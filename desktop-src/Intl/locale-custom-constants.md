---
description: Constantes personalizadas de configuración regional \_ \*
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: Constantes de LOCALE_CUSTOM *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4e02cc672241fd609a5eda975c0e9e13d29908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686504"
---
# <a name="locale_custom-constants"></a>Constantes personalizadas de configuración regional \_ \*

En este tema se definen las \_ constantes personalizadas de configuración regional \* utilizadas por NLS para representar [configuraciones regionales personalizadas](custom-locales.md).



| Value                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONFIGURACIÓN \_ predeterminada personalizada \_     | **Windows Vista y versiones posteriores:** Configuración regional personalizada predeterminada. Cuando una función NLS debe devolver un identificador de configuración regional para una [configuración regional complementaria](custom-locales.md) para el usuario actual, la función devuelve este valor en lugar del valor [predeterminado del \_ usuario \_ de la configuración regional](locale-user-default.md). El valor predeterminado de configuración \_ regional \_ es 0x0C00.                                                                                                                                                                  |
| CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_ | **Windows Vista y versiones posteriores:** Configuración regional personalizada predeterminada para MUI. Los idiomas de interfaz de usuario preferidos del usuario y los idiomas de interfaz de usuario preferidos del sistema pueden incluir como máximo un solo idioma que se implementa mediante un paquete de interfaz de idiomas (LIP) y para el que el identificador de idioma corresponde a una configuración regional complementaria. Si hay un lenguaje tal en una lista, la constante se usa para hacer referencia a ese idioma en determinados contextos. El valor predeterminado de la configuración regional de la \_ \_ interfaz de usuario personalizada \_ es 0x1400.                    |
| configuración regional \_ personalizada no \_ especificada | **Windows Vista y versiones posteriores:** Una configuración regional personalizada no especificada, que se usa para identificar todas las configuraciones regionales complementarias excepto la configuración regional del usuario actual. Las configuraciones regionales complementarias no se pueden distinguir unas de otras por sus identificadores de configuración regional, pero se pueden distinguir por sus [nombres de configuración regional](locale-names.md). Ciertas funciones NLS pueden devolver esta constante para indicar que no pueden proporcionar un identificador útil para una configuración regional concreta. El valor de configuración regional \_ personalizada \_ sin especificar es 0x1000. |



 

 

 



