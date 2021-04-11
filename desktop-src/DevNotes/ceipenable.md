---
description: HKLM \\ software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7b86a726af95e7ec9fb764d5e752057a24b3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274929"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Tipo de datos  | Intervalo                     | Valor predeterminado |
|------------|---------------------------|---------------|
| \_valor DWORD reg | 0 (deshabilitar) o 1 (habilitar) | 0             |



 

## <a name="description"></a>Descripción

Habilita el programa para la mejora de la experiencia del usuario de Windows.

## <a name="change-method"></a>Cambiar método

Para cambiar el valor de esta entrada, en el panel de control, seleccione **sistema y mantenimiento**, seguido de **informes de problemas y soluciones**. Haga clic en configuración de la mejora de la **experiencia del usuario** en la sección Vea también.

## <a name="activation-method"></a>Método de activación

Los cambios realizados en esta entrada entran en vigor de forma inmediata. Al habilitar esta clave del registro, se habilitará la Programa para la mejora de la experiencia del usuario de Windows para todo el equipo. Al deshabilitar esta clave del registro, se deshabilitará la Programa para la mejora de la experiencia del usuario de Windows para todo el equipo.

Esta entrada se puede sustituir por un valor de directiva de grupo en los sistemas que admiten directiva de grupo. Mientras está habilitada la opción directiva de grupo de Windows Programa para la mejora de la experiencia del usuario CEIP habilitar, el sistema omite esta entrada. La configuración de esta configuración de Directiva se almacena en la sección **directivas** en **HKLM \\ software \\ Policies \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



