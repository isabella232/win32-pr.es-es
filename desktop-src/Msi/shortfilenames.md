---
description: El establecimiento de la propiedad SHORTFILENAMES hace que se usen nombres de archivo cortos para los nombres de archivos de destino, en lugar de nombres de archivo largos. No afecta a los nombres de archivo que busca el instalador en el origen.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654003"
---
# <a name="shortfilenames-property"></a>SHORTFILENAMES (propiedad)

El establecimiento de la propiedad **SHORTFILENAMES** hace que se usen nombres de archivo cortos para los nombres de archivos de destino, en lugar de nombres de archivo largos. No afecta a los nombres de archivo que busca el instalador en el origen.

## <a name="default-value"></a>Valor predeterminado

El instalador usa nombres largos si no se establece la propiedad **SHORTFILENAMES** y el volumen de destino admite nombres largos. El instalador usa nombres cortos si el volumen de destino no admite nombres largos.

## <a name="remarks"></a>Observaciones

Cuando se establece la propiedad **SHORTFILENAMES** , el instalador crea carpetas e instala archivos mediante nombres de archivo cortos a partir de los \| pares largos cortos enumerados en la tabla de [archivos](file-table.md) o en la [tabla de directorios](directory-table.md).

Las aplicaciones pueden usar la función [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) para recuperar el formato de ruta de acceso abreviada de una ruta de acceso de archivo especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
