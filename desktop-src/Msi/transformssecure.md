---
description: Al establecer la propiedad TRANSFORMSSECURE en 1, se informa al instalador de que las transformaciones se almacenarán en caché localmente en el equipo del usuario en una ubicación donde el usuario no tenga acceso de escritura.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propiedad TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af3432b8f895d4d9f5d0fe643ef8106e01e28ad64fb2db177e968fbc13d88de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141638"
---
# <a name="transformssecure-property"></a>Propiedad TRANSFORMSSECURE

Al establecer la propiedad **TRANSFORMSSECURE** en 1, se informa al instalador de que las transformaciones se almacenarán en caché localmente en el equipo del usuario en una ubicación donde el usuario no tenga acceso de escritura. Establecer esta propiedad es como establecer la [directiva TransformsSecure,](transformssecure-policy.md) salvo que el ámbito es diferente. El establecimiento de la directiva TransformsSecure se aplica a todos los paquetes instalados por un usuario determinado. El establecimiento **de la propiedad TRANSFORMSSECURE** se aplica al paquete independientemente del usuario.

El propósito de esta propiedad es proporcionar almacenamiento de transformación seguro con usuarios que viajan Windows 2000. Cuando se establece esta propiedad, una [instalación de mantenimiento](maintenance-installation.md) solo puede usar la transformación de la ruta de acceso especificada. Si la ruta de acceso no está disponible, se produce un error en la instalación de mantenimiento. Por lo tanto, un origen para cada transformación segura debe residir en la ubicación del origen del paquete de instalación. A continuación, si el instalador encuentra que falta la transformación en el equipo local, puede restaurar la transformación desde este origen.

## <a name="remarks"></a>Comentarios

Windows El instalador interpreta que [**la propiedad TRANSFORMSATSOURCE**](transformsatsource.md) es la misma que la **propiedad TRANSFORMSSECURE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> </dl>

 

 




