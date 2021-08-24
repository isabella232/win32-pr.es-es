---
description: Establecer el valor de esta directiva de sistema por máquina en \# &0034;1&0034; evita que los usuarios no administradores usen un cuadro de diálogo Examinar para buscar orígenes de aplicaciones administradas almacenadas en medios, como \# CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e565cca833d8d771b5bc28dea4483049868995a06acc9a42116611a1df6ce098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745575"
---
# <a name="disablebrowse"></a>DisableBrowse

Establecer el valor de [](system-policy.md) esta directiva de sistema por equipo en "1" impide [que](browse-dialog.md) [](m-gly.md) los usuarios no administradores usen un cuadro de diálogo Examinar para buscar orígenes de aplicaciones administradas almacenadas en medios, como CD-ROM. El cuadro combinado "Usar característica de:" para la entrada directa está bloqueado y "Examinar..." el botón está deshabilitado. Para obtener más detalles sobre la exploración del origen, vea [resistencia de origen.](source-resiliency.md)

DisableBrowse invalida AllowLockdownBrowse e impide la exploración incluso si se establece AllowLockdownBrowse.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Comentarios

En algunos casos con DisableBrowse establecido, un usuario no administrador puede seguir siendo capaz de instalar aplicaciones administradas desde orígenes en medios etiquetados correctamente. Al establecer la directiva DisableBrowse solo se deshabilita la capacidad de ir a los orígenes. Se puede usar para evitar que un usuario no administrador se desentrase de un nuevo origen durante una instalación, reinstalación o reparación a petición. Si [se establece AllowLockdownMedia,](allowlockdownmedia.md) el usuario no administrador podría seguir instalando una aplicación administrada desde medios etiquetados correctamente.

DisableBrowse impide que el usuario no administrador se desasocia a una nueva ubicación multimedia o a cualquier otra ubicación de origen. Para más información sobre cómo proteger los orígenes multimedia de las aplicaciones administradas, consulte [Resistencia de origen.](source-resiliency.md)

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, vea [Administrar orígenes de instalación](managing-installation-sources.md).

 

 



