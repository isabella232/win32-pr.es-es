---
description: Establecer el valor de esta directiva de sistema por máquina en \# &0034;1&0034; permite a los usuarios no administradores instalar aplicaciones administradas desde orígenes almacenados en medios, como \# un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159150"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

Al establecer el valor [](system-policy.md) de esta directiva de sistema por máquina en "1", los usuarios no administradores pueden instalar aplicaciones administradas desde orígenes almacenados en medios, como un CD-ROM. [](m-gly.md) Vea [Resistencia de origen.](source-resiliency.md) Por ejemplo, si se establece esta directiva, un usuario no administrador puede usar un origen multimedia para instalar aplicaciones o aplicaciones asignadas o publicadas que se instalan para todos los usuarios. Establecer esta directiva también permite a los usuarios no administrativos ejecutar programas con privilegios LocalSystem durante una instalación con privilegios elevados.

El valor predeterminado de esta directiva es 1 solo en equipos que ejecutan Windows Vista y que no están unidos a un dominio. El valor predeterminado en otros equipos es que los usuarios no administradores no pueden instalar aplicaciones administradas desde un origen ubicado en medios.

Dado que esta directiva permite a los usuarios que no son administradores instalar con privilegios que no tienen de forma predeterminada, antes de establecer esta directiva debe considerar si proporciona un nivel de seguridad adecuado para el usuario. Se recomienda la configuración predeterminada para garantizar un entorno seguro.

Para obtener más información sobre cómo proteger las instalaciones y el uso de certificados digitales, vea [Directrices](guidelines-for-authoring-secure-installations.md) para crear instalaciones [seguras](digital-signatures-and-windows-installer.md) y firmas digitales y Windows Installer y Descargar una instalación [desde Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Observaciones

Establecer esta directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios con privilegios LocalSystem si tienen un paquete del instalador de Windows que instala o inicia esos programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



