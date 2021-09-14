---
description: Establecer esta propiedad es como establecer la directiva de directiva TransformsAtSource, salvo que el ámbito es diferente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: TransformSATSOURCE, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071831"
---
# <a name="transformsatsource-property"></a>TransformSATSOURCE, propiedad

Establecer esta propiedad es como establecer la directiva de directiva [TransformsAtSource,](transformsatsource-policy.md) salvo que el ámbito es diferente. La configuración de la directiva TransformsAtSource se aplica a todos los paquetes instalados por un usuario determinado. El establecimiento **de la propiedad TRANSFORMSATSOURCE** se aplica al paquete independientemente de los usuarios.

## <a name="remarks"></a>Observaciones

Windows El instalador interpreta la **propiedad TRANSFORMSATSOURCE** como si fuera la [**propiedad TRANSFORMSSECURE.**](transformssecure.md) Si se pasa la marca @ en la propiedad [**TRANSFORMS,**](transforms.md) Windows Installer trata las transformaciones de la lista como transformaciones [seguras en el origen.](secure-at-source-transforms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




