---
description: AdminProperties debe crearse en la tabla de propiedades.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propiedad AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f59d2452e244bd22110ab918dff61279bf9d27f3c8735f37474aea894d0d02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078135"
---
# <a name="adminproperties-property"></a>Propiedad AdminProperties

AdminProperties **debe** crearse en la tabla [de propiedades](property-table.md). El valor de **AdminProperties** es una lista de nombres de propiedad separados por punto y coma. El instalador guarda los valores de estas propiedades enumeradas en el momento de una [instalación administrativa.](administrative-installation.md) Cuando los usuarios instalan desde la imagen administrativa, la instalación usa los valores guardados de las propiedades, en lugar de los valores del .msi archivo.

## <a name="remarks"></a>Comentarios

Los nombres de propiedad de la lista pueden estar en mayúsculas y minúsculas (propiedades privadas) o en mayúsculas (propiedades públicas).

Esta propiedad nunca debe terminar con un punto y coma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




