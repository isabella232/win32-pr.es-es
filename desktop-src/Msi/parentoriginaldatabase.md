---
description: Durante una instalación simultánea, el instalador establece la propiedad ParentOriginalDatabase de la sesión de la instalación simultánea en el mismo valor que la propiedad OriginalDatabase de la sesión de la instalación primaria.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: ParentOriginalDatabase, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31d022aa4ec7274d464943d8b3ec059ce11142f06e0e09c22bbb42ec40a2e5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913275"
---
# <a name="parentoriginaldatabase-property"></a>ParentOriginalDatabase, propiedad

Durante una instalación simultánea, el instalador establece la propiedad **ParentOriginalDatabase** de la sesión de la instalación simultánea en el mismo valor que la propiedad [**OriginalDatabase**](originaldatabase.md) de la sesión de la instalación primaria. Las instalaciones primarias usan las acciones de instalación simultáneas para realizar una instalación simultánea. Un paquete de instalación puede determinar si se instala mediante una acción de instalación simultánea comprobando el valor de esta propiedad.

> [!Note]  
> No se recomiendan instalaciones simultáneas para la instalación de aplicaciones diseñadas para su lanzamiento al público. Para obtener información sobre las instalaciones simultáneas, vea [Instalaciones simultáneas.](concurrent-installations.md)

 

> [!Note]  
> Esta propiedad no se establece si la acción [RemoveExistingProducts](removeexistingproducts-action.md) ejecuta la instalación simultánea.

 

## <a name="remarks"></a>Comentarios

Para evitar que un paquete se instale como una instalación simultánea, agregue cualquiera de las siguientes instrucciones condicionales a la [tabla LaunchCondition.](launchcondition-table.md) Esto evita que el paquete se instale alguna vez mediante una acción de instalación simultánea ejecutada por otra instalación. Esto no impide que la acción [RemoveExistingProducts](removeexistingproducts-action.md) instale el paquete.

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




