---
description: Establecer el valor de esta Directiva del sistema por equipo en &\# 0034; 1&\# 0034; permite a los usuarios no administrativos usar un cuadro de diálogo examinar para buscar orígenes de aplicaciones administradas.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909117"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

Establecer el valor de esta [Directiva del sistema](system-policy.md) por equipo en "1" permite a los usuarios no administrativos usar un [cuadro de diálogo examinar](browse-dialog.md) para buscar orígenes de [*aplicaciones administradas*](m-gly.md). Los orígenes pueden incluir medios, como CD-ROM, direcciones URL y ubicaciones de red. Para obtener más información, consulte [resistencia del origen](source-resiliency.md). El valor predeterminado en Windows Installer es que los usuarios no administrativos no pueden buscar nuevos orígenes de aplicaciones administradas. Los únicos orígenes disponibles son aquellos que ya están registrados en la lista de origen del producto. Si se establece esta Directiva, un usuario no administrativo puede buscar nuevos orígenes de aplicaciones asignadas o publicadas o aplicaciones instaladas para todos los usuarios. La configuración de AllowLockdownBrowse también permite a los usuarios no administrativos ejecutar programas en privilegios LocalSystem durante una instalación con privilegios elevados.

Se recomienda la configuración predeterminada para garantizar un entorno seguro.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios en privilegios LocalSystem si tienen un paquete de Windows Installer que instala o inicia esos programas.

[DisableBrowse](disablebrowse.md) invalida AllowLockdownBrowse y evita que se examine incluso si AllowLockdownBrowse está establecido.

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, consulte [Administración de orígenes de instalación](managing-installation-sources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 



