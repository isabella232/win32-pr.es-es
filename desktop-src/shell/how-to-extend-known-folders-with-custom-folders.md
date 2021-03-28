---
description: Los fabricantes de software independientes (ISV) pueden extender el conjunto de carpetas conocidas en un sistema mediante el registro de carpetas conocidas propias.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Cómo extender carpetas conocidas con carpetas personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276748"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Cómo extender carpetas conocidas con carpetas personalizadas

Los fabricantes de software independientes (ISV) pueden extender el conjunto de carpetas conocidas en un sistema mediante el registro de carpetas conocidas propias. Una vez registrada, el sistema conoce esas carpetas de terceros. Los encuentra cualquier llamada a [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Tenga en cuenta que una carpeta conocida debe ser una carpeta por equipo. No se puede crear una carpeta conocida por usuario.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Defina la carpeta conocida a través de una estructura de [**\_ definición de KNOWNFOLDER**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .

### <a name="step-2"></a>Paso 2:

Registre la carpeta conocida a través de una llamada a [**IKnownFolderManager:: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Observaciones

Si crea una carpeta conocida para la aplicación como parte del procedimiento de instalación, también debe incluir [**IKnownFolderManager:: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) como parte del código de desinstalación.

Tenga en cuenta el motivo por el que desea que la carpeta se incluya en el sistema de carpetas conocidas antes de registrarla. Debe tener un motivo válido para elevar la carpeta a ese nivel de visibilidad del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
