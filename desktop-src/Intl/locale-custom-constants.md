---
description: Constantes CUSTOM de LOCALE \_ \*
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: LOCALE_CUSTOM* Constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc2bebc121ad2db797a2ff80b1fee925fc529cd3129ce6b906a579788789899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106895"
---
# <a name="locale_custom-constants"></a>Constantes CUSTOM de LOCALE \_ \*

En este tema se definen las constantes CUSTOM de LOCALE usadas por \_ \* NLS para representar [configuraciones regionales personalizadas.](custom-locales.md)



| Value                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONFIGURACIÓN REGIONAL \_ PREDETERMINADA \_ PERSONALIZADA     | **Windows Vista y versiones posteriores:** Configuración regional personalizada predeterminada. Cuando una función NLS debe devolver un identificador de configuración regional para una configuración [regional](custom-locales.md) complementaria para el usuario actual, la función devuelve este valor en lugar de [LOCALE \_ USER \_ DEFAULT](locale-user-default.md). El valor de LOCALE \_ CUSTOM \_ DEFAULT es 0x0C00.                                                                                                                                                                  |
| CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DE LA INTERFAZ DE USUARIO \_ \_ PERSONALIZADA | **Windows Vista y versiones posteriores:** Configuración regional personalizada predeterminada para MUI. Los idiomas de interfaz de usuario preferidos por el usuario y los idiomas de interfaz de usuario preferidos del sistema pueden incluir como máximo un único idioma implementado por un Paquete de interfaz de idiomas (LIP) y para el que el identificador de idioma corresponde a una configuración regional complementaria. Si hay un idioma de este tipo en una lista, la constante se usa para hacer referencia a ese idioma en determinados contextos. El valor de LOCALE \_ CUSTOM UI DEFAULT es \_ \_ 0x1400.                    |
| CONFIGURACIÓN REGIONAL \_ PERSONALIZADA \_ SIN ESPECIFICAR | **Windows Vista y versiones posteriores:** Configuración regional personalizada no especificada, que se usa para identificar todas las configuraciones regionales complementarias excepto la configuración regional del usuario actual. Las configuraciones regionales complementarias no se pueden distinguir entre sí por sus identificadores de configuración regional, pero se pueden distinguir por sus nombres [de configuración regional.](locale-names.md) Algunas funciones NLS pueden devolver esta constante para indicar que no pueden proporcionar un identificador útil para una configuración regional determinada. El valor de LOCALE \_ CUSTOM \_ UNSPECIFIED es 0x1000. |



 

 

 



