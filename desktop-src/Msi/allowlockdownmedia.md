---
description: Establecer el valor de esta Directiva del sistema por equipo en &\# 0034; 1&\# 0034; permite a los usuarios no administrativos instalar aplicaciones administradas desde orígenes almacenados en medios, como un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914222"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

Establecer el valor de esta [Directiva del sistema](system-policy.md) por equipo en "1" permite a los usuarios no administrativos instalar [*aplicaciones administradas*](m-gly.md) desde orígenes almacenados en medios, como un CD-ROM. Consulte [resistencia del origen](source-resiliency.md). Por ejemplo, si se establece esta Directiva, un usuario no administrativo puede usar un origen de medios para instalar aplicaciones asignadas o publicadas o aplicaciones que se instalan para todos los usuarios. La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas en privilegios LocalSystem durante una instalación con privilegios elevados.

El valor predeterminado de esta directiva es 1 solo en los equipos que ejecutan Windows Vista y que no están Unidos a un dominio. El valor predeterminado en otros equipos es que los usuarios no administrativos no pueden instalar aplicaciones administradas desde un origen ubicado en un medio.

Dado que esta directiva permite a los usuarios que no son administradores instalar con privilegios que no tienen de forma predeterminada, antes de establecer esta Directiva debe considerar si proporciona un nivel de seguridad adecuado para el usuario. Se recomienda la configuración predeterminada para garantizar un entorno seguro.

Para obtener más información acerca de la protección de instalaciones y el uso de certificados digitales, consulte [directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md) y [descargar una instalación desde Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios en privilegios LocalSystem si tienen un paquete de Windows Installer que instala o inicia esos programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



