---
description: Establecer esta propiedad es como establecer la directiva de directiva TransformsAtSource, salvo que el ámbito es diferente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: TransformSATSOURCE, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f48f34f52bf76a9aca07b7b41d18f666543b1afcc6332a227c951344dcf905
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500304"
---
# <a name="transformsatsource-property"></a>TransformSATSOURCE, propiedad

Establecer esta propiedad es como establecer la directiva de directiva [TransformsAtSource,](transformsatsource-policy.md) salvo que el ámbito es diferente. La configuración de la directiva TransformsAtSource se aplica a todos los paquetes instalados por un usuario determinado. El establecimiento **de la propiedad TRANSFORMSATSOURCE** se aplica al paquete independientemente de los usuarios.

## <a name="remarks"></a>Comentarios

Windows El instalador interpreta la **propiedad TRANSFORMSATSOURCE** como si fuera la [**propiedad TRANSFORMSSECURE.**](transformssecure.md) Si se pasa la marca @ en la propiedad [**TRANSFORMS,**](transforms.md) Windows Installer trata las transformaciones de la lista como transformaciones [seguras en origen.](secure-at-source-transforms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




