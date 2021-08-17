---
description: Los proveedores de software independientes (ISV) pueden ampliar el conjunto de carpetas conocidas en un sistema mediante el registro de carpetas conocidas propias.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Cómo ampliar carpetas conocidas con carpetas personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a04a5ef10c8e3ee909944e6782cf32ca6aa2aa6b50e03f018f31a6aafe529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350875"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Cómo ampliar carpetas conocidas con carpetas personalizadas

Los proveedores de software independientes (ISV) pueden ampliar el conjunto de carpetas conocidas en un sistema mediante el registro de carpetas conocidas propias. Una vez registradas, el sistema conoce esas carpetas de terceros. Se encuentran mediante cualquier llamada a [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Tenga en cuenta que una carpeta conocida debe ser una carpeta por equipo. No se puede crear una carpeta conocida por usuario.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Defina la carpeta conocida mediante una [**estructura KNOWNFOLDER \_ DEFINITION.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition)

### <a name="step-2"></a>Paso 2:

Registre la carpeta conocida mediante una llamada a [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Comentarios

Si crea una carpeta conocida para la aplicación como parte del procedimiento de instalación, también debe incluir [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) como parte del código de desinstalación.

Tenga en cuenta por qué quiere que la carpeta se incluya en el sistema de carpetas conocido antes de registrarla. Debe tener un motivo válido para elevar la carpeta a ese nivel de visibilidad del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
