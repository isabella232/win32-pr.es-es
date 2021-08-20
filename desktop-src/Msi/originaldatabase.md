---
description: El Windows establece la propiedad OriginalDatabase en la ruta de acceso de la base de datos de instalación utilizada para iniciar la instalación.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propiedad OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b8ec6b77d013ee89d081c0ff20e3ad00750454e1fa9299d364fdb94e69ccb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145538"
---
# <a name="originaldatabase-property"></a>Propiedad OriginalDatabase

El Windows de instalación establece la **propiedad OriginalDatabase** en la ruta de acceso de la base de datos de instalación utilizada para iniciar la instalación. Si la instalación se inicia desde una línea de comandos, el valor depende de si la opción de paquete recache (la marca -v) está presente en la [**propiedad REINSTALLMODE.**](reinstallmode.md)



| Método de instalación                                                                                                                                                                                  | Valor originalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Cualquier instalación iniciada invocando la ruta de acceso del paquete de instalación (.msi archivo).                                                                                                              | Ruta de acceso al paquete de instalación (.msi archivo). |
| Instalación iniciada desde una línea de comandos. La instalación no se inicia desde una ruta de acceso del paquete. La opción recache (marca -v) está presente en la [**propiedad REINSTALLMODE.**](reinstallmode.md)     | Ruta de acceso a la base de datos en el origen.           |
| Instalación iniciada desde una línea de comandos. La instalación no se inicia desde una ruta de acceso del paquete. La opción recache (marca -v) no está presente en la [**propiedad REINSTALLMODE.**](reinstallmode.md) | Ruta de acceso a la base de datos almacenada en caché.                  |



 

## <a name="remarks"></a>Comentarios

Durante la primera instalación, una acción personalizada secuenciada antes de la acción [ResolveSource](resolvesource-action.md) puede usar la **propiedad OriginalDatabase** para determinar la ubicación del origen de instalación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




