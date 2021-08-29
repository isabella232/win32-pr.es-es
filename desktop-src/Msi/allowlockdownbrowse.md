---
description: Establecer el valor de esta directiva de sistema por máquina en \# &0034;1&0034; permite a los usuarios no administradores usar un cuadro de diálogo Examinar para buscar orígenes de aplicaciones \# administradas.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9af9f2c5eb4c455c9eeb0cc2f24abb674a84647b5616752afdc3b277c73b1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821975"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

Establecer el valor de [](system-policy.md) esta directiva de sistema por equipo en "1" permite [a](browse-dialog.md) los usuarios no administradores usar un cuadro de diálogo Examinar para buscar orígenes de [*aplicaciones administradas.*](m-gly.md) Los orígenes pueden incluir medios, como CD-ROM, direcciones URL y ubicaciones de red. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md) El valor predeterminado de Windows Installer es que los usuarios no administradores no pueden buscar nuevos orígenes de aplicaciones administradas. Los únicos orígenes disponibles son los que ya están registrados en la lista de origen del producto. Si se establece esta directiva, un usuario no administrador puede buscar nuevos orígenes de aplicaciones o aplicaciones asignadas o publicadas que se instalan para todos los usuarios. Establecer AllowLockdownBrowse también permite a los usuarios no administrativos ejecutar programas con privilegios LocalSystem durante una instalación con privilegios elevados.

Se recomienda la configuración predeterminada para garantizar un entorno seguro.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Comentarios

Establecer esta directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios con privilegios LocalSystem si tienen un paquete del instalador de Windows que instala o inicia esos programas.

[DisableBrowse invalida](disablebrowse.md) AllowLockdownBrowse e impide la exploración aunque se establezca AllowLockdownBrowse.

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, vea [Administrar orígenes de instalación](managing-installation-sources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 



