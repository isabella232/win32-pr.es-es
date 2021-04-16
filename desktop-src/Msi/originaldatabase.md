---
description: El Windows Installer establece la propiedad OriginalDatabase en la ruta de acceso de la base de datos de instalación que se usa para iniciar la instalación.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propiedad OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679525"
---
# <a name="originaldatabase-property"></a>Propiedad OriginalDatabase

El Windows Installer establece la propiedad **OriginalDatabase** en la ruta de acceso de la base de datos de instalación que se usa para iniciar la instalación. Si la instalación se inicia desde una línea de comandos, el valor depende de si la opción de paquete para volver a almacenar en caché (la marca-v) está presente en la propiedad [**REINSTALLMODE**](reinstallmode.md) .



| Método de instalación                                                                                                                                                                                  | Valor OriginalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Cualquier instalación iniciada mediante la invocación de la ruta de acceso del paquete de instalación (archivo. msi).                                                                                                              | Ruta de acceso al paquete de instalación (archivo. msi). |
| Instalación iniciada desde una línea de comandos. La instalación no se inicia desde una ruta de acceso del paquete. La opción recache (-v flag) está presente en la propiedad [**REINSTALLMODE**](reinstallmode.md) .     | Ruta de acceso a la base de datos en el origen.           |
| Instalación iniciada desde una línea de comandos. La instalación no se inicia desde una ruta de acceso del paquete. La opción recache (-v flag) no está presente en la propiedad [**REINSTALLMODE**](reinstallmode.md) . | Ruta de acceso a la base de datos almacenada en caché.                  |



 

## <a name="remarks"></a>Observaciones

Durante una instalación por primera vez, una acción personalizada se secuencia antes de la [acción ResolveSource](resolvesource-action.md) puede usar la propiedad **OriginalDatabase** para determinar la ubicación del origen de instalación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




