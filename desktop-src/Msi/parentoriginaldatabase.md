---
description: Durante una instalación simultánea, el instalador establece la propiedad ParentOriginalDatabase en la sesión de la instalación simultánea en el mismo valor que la propiedad OriginalDatabase de la sesión de la instalación primaria.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Propiedad ParentOriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653768"
---
# <a name="parentoriginaldatabase-property"></a>Propiedad ParentOriginalDatabase

Durante una instalación simultánea, el instalador establece la propiedad **ParentOriginalDatabase** en la sesión de la instalación simultánea en el mismo valor que la propiedad [**OriginalDatabase**](originaldatabase.md) de la sesión de la instalación primaria. Las instalaciones primarias usan las acciones de instalación simultáneas para realizar una instalación simultánea. Un paquete de instalación puede determinar si se está instalando mediante una acción de instalación simultánea comprobando el valor de esta propiedad.

> [!Note]  
> No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.

 

> [!Note]  
> Esta propiedad no se establece si la acción [RemoveExistingProducts](removeexistingproducts-action.md) ejecuta la instalación simultánea.

 

## <a name="remarks"></a>Observaciones

Para evitar que un paquete se instale una vez como una instalación simultánea, agregue cualquiera de las siguientes instrucciones condicionales a la tabla [LaunchCondition](launchcondition-table.md) . Esto evita que el paquete se instale una acción de instalación simultánea ejecutada por otra instalación. Esto no impide que el paquete se instale mediante la acción [RemoveExistingProducts](removeexistingproducts-action.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




