---
description: La propiedad SourceDir es el directorio raíz que contiene el archivo. cab de origen o el árbol de archivos de origen del paquete de instalación. Este valor se usa para la resolución de directorios.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Propiedad SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681042"
---
# <a name="sourcedir-property"></a>Propiedad SourceDir

La propiedad **SourceDir** es el directorio raíz que contiene el archivo. cab de origen o el árbol de archivos de origen del paquete de instalación. Este valor se usa para la resolución de directorios.

## <a name="default-value"></a>Valor predeterminado

Directorio que contiene el paquete de instalación.

## <a name="remarks"></a>Observaciones

Se debe llamar a la [acción ResolveSource](resolvesource-action.md) antes de usar la propiedad **SourceDir** en cualquier expresión o intentar recuperar el valor de **SourceDir** con [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). La acción ResolveSource no debe ejecutarse mientras el origen no esté disponible, por ejemplo, al desinstalar una aplicación, ya que esto puede producir un mensaje imprevisto para los medios de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




