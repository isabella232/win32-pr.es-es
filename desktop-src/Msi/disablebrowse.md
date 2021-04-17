---
description: Al establecer el valor de esta Directiva del sistema por equipo en &\# 0034; 1&\# 0034; se impide que los usuarios no administrativos utilicen un cuadro de diálogo examinar para buscar orígenes de aplicaciones administradas almacenadas en medios, como un CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652371"
---
# <a name="disablebrowse"></a>DisableBrowse

Al establecer el valor de esta [Directiva del sistema](system-policy.md) por equipo en "1", se impide que los usuarios no administrativos utilicen un [cuadro de diálogo examinar](browse-dialog.md) para buscar orígenes de [*aplicaciones administradas*](m-gly.md) almacenadas en medios, como un CD-ROM. El cuadro combinado "usar característica de:" para entrada directa está bloqueado y el "examinar..." el botón está deshabilitado. Para obtener más información sobre la exploración de código fuente, consulte [resistencia de origen](source-resiliency.md).

DisableBrowse invalida AllowLockdownBrowse y evita que se examine incluso si AllowLockdownBrowse está establecido.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

En algunos casos con DisableBrowse establecido, un usuario no administrativo puede seguir pudiendo instalar aplicaciones administradas desde orígenes en medios etiquetados correctamente. La configuración de la Directiva DisableBrowse solo deshabilita la capacidad de examinar los orígenes. Se puede usar para impedir que un usuario no administrativo navegue a un nuevo origen durante una instalación, reinstalación o reparación a petición. Si se establece [AllowLockdownMedia](allowlockdownmedia.md) , el usuario no administrativo podría seguir instalando una aplicación administrada desde un medio etiquetado correctamente.

DisableBrowse impide que el usuario no administrativo navegue a una nueva ubicación de medios o a cualquier otra ubicación de origen. Para obtener más información sobre cómo proteger los orígenes multimedia de las aplicaciones administradas, consulte [resistencia del origen](source-resiliency.md).

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, consulte [Administración de orígenes de instalación](managing-installation-sources.md).

 

 



