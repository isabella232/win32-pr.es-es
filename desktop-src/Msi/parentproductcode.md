---
description: Durante una instalación simultánea, el instalador establece la propiedad ParentProductCode de la sesión de la instalación simultánea en el mismo valor que la propiedad ProductCode de la sesión de la instalación primaria.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Propiedad ParentProductCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250928"
---
# <a name="parentproductcode-property"></a>Propiedad ParentProductCode

Durante una instalación simultánea, el instalador establece la propiedad **ParentProductCode** de la sesión de la instalación simultánea en el mismo valor que la propiedad [**ProductCode**](productcode.md) de la sesión de la instalación primaria. Las instalaciones primarias ejecutan las acciones de instalación simultáneas para realizar una instalación simultánea. Un paquete de instalación puede determinar si se instala mediante una acción de instalación simultánea comprobando el valor de esta propiedad.

> [!Note]  
> No se recomiendan las instalaciones simultáneas para la instalación de aplicaciones diseñadas para su lanzamiento al público. Para obtener información sobre las instalaciones simultáneas, vea [Instalaciones simultáneas.](concurrent-installations.md)

 

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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**ParentOriginalDatabase**](parentoriginaldatabase.md)
</dt> </dl>

 

 




