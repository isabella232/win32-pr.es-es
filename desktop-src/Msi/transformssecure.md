---
description: Al establecer la propiedad TRANSFORMSSECURE en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propiedad TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681117"
---
# <a name="transformssecure-property"></a>Propiedad TRANSFORMSSECURE

Al establecer la propiedad **TRANSFORMSSECURE** en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura. Establecer esta propiedad es como establecer la [Directiva TransformsSecure](transformssecure-policy.md) , salvo que el ámbito es diferente. La configuración de la Directiva TransformsSecure se aplica a todos los paquetes instalados por un usuario determinado. El establecimiento de la propiedad **TRANSFORMSSECURE** se aplica al paquete independientemente del usuario.

El propósito de esta propiedad es proporcionar almacenamiento de transformación seguro con usuarios móviles de Windows 2000. Cuando se establece esta propiedad, una [instalación de mantenimiento](maintenance-installation.md) solo puede utilizar la transformación de la ruta de acceso especificada. Si la ruta de acceso no está disponible, se produce un error en la instalación del mantenimiento. Por tanto, un origen para cada transformación segura debe residir en la ubicación del origen del paquete de instalación. Después, si el instalador detecta que falta la transformación en el equipo local, puede restaurar la transformación desde este origen.

## <a name="remarks"></a>Observaciones

Windows Installer interpreta la propiedad [**TRANSFORMSATSOURCE**](transformsatsource.md) para que sea igual que la propiedad **TRANSFORMSSECURE** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> </dl>

 

 




