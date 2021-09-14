---
description: Durante una instalación simultánea, el instalador establece la propiedad ParentOriginalDatabase de la sesión de la instalación simultánea en el mismo valor que la propiedad OriginalDatabase de la sesión de la instalación primaria.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: ParentOriginalDatabase, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250935"
---
# <a name="parentoriginaldatabase-property"></a>ParentOriginalDatabase, propiedad

Durante una instalación simultánea, el instalador establece la propiedad **ParentOriginalDatabase** de la sesión de la instalación simultánea en el mismo valor que la propiedad [**OriginalDatabase**](originaldatabase.md) de la sesión de la instalación primaria. Las instalaciones primarias usan las acciones de instalación simultáneas para realizar una instalación simultánea. Un paquete de instalación puede determinar si se está instalando mediante una acción de instalación simultánea comprobando el valor de esta propiedad.

> [!Note]  
> No se recomiendan las instalaciones simultáneas para la instalación de aplicaciones destinadas a la versión pública. Para obtener información sobre las instalaciones simultáneas, vea [Instalaciones simultáneas.](concurrent-installations.md)

 

> [!Note]  
> Esta propiedad no se establece si la acción [RemoveExistingProducts](removeexistingproducts-action.md) ejecuta la instalación simultánea.

 

## <a name="remarks"></a>Observaciones

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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




