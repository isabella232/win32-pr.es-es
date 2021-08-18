---
description: HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687e17bf5438406fb7a29b954bf8a2640fc0ea5d193ba49ae7fd7bd02f1f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956124"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Tipo de datos  | Intervalo                     | Valor predeterminado |
|------------|---------------------------|---------------|
| REG \_ DWORD | 0 (deshabilitar) o 1 (habilitar) | 0             |



 

## <a name="description"></a>Descripción

Habilita el programa Windows mejora de la experiencia del usuario.

## <a name="change-method"></a>Cambiar método

Para cambiar el valor de esta entrada, en Panel de control, seleccione Sistema y **mantenimiento,** seguido de **Informes de problemas y Soluciones.** Haga clic en Customer Experience Improvement Configuración (Mejora de la experiencia del **usuario)** en la sección Consulte también.

## <a name="activation-method"></a>Método de activación

Los cambios realizados en esta entrada son efectivos inmediatamente. Al habilitar esta clave del Registro, Windows Programa para la mejora de la experiencia del usuario se habilita para todo el equipo. Al deshabilitar esta clave del Registro, Windows Programa para la mejora de la experiencia del usuario se deshabilita para todo el equipo.

Esta entrada se puede sustituir por una configuración directiva de grupo en sistemas que admiten directiva de grupo. Si bien la Windows Programa para la mejora de la experiencia del usuario configuración de directiva de grupo la opción Habilitar CEIP está habilitada, el sistema omite esta entrada. La configuración de esta configuración de directiva se almacena en la sección **Directivas** en **HKLM \\ Software Policies \\ Microsoft \\ \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



