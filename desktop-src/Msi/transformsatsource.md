---
description: El establecimiento de esta propiedad es como establecer la Directiva de directiva TransformsAtSource, excepto que el ámbito es diferente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Propiedad TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681116"
---
# <a name="transformsatsource-property"></a>Propiedad TRANSFORMSATSOURCE

El establecimiento de esta propiedad es como establecer la Directiva de [Directiva TransformsAtSource](transformsatsource-policy.md) , excepto que el ámbito es diferente. La configuración de la Directiva TransformsAtSource se aplica a todos los paquetes instalados por un usuario determinado. El establecimiento de la propiedad **TRANSFORMSATSOURCE** se aplica al paquete, independientemente de los usuarios.

## <a name="remarks"></a>Observaciones

Windows Installer interpreta la propiedad **TRANSFORMSATSOURCE** como si fuera la propiedad [**TRANSFORMSSECURE**](transformssecure.md) . Si se pasa la marca @ en la propiedad [**TRANSformations**](transforms.md) , Windows Installer trata las transformaciones de la lista como [transformaciones seguras en el origen](secure-at-source-transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




