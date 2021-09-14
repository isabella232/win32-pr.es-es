---
description: Establecer la propiedad SHORTFILENAMES hace que se utilicen nombres de archivo cortos para los nombres de los archivos de destino, en lugar de nombres de archivo largos. No afecta a los nombres de archivo que busca el instalador en el origen.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074296"
---
# <a name="shortfilenames-property"></a>SHORTFILENAMES, propiedad

Establecer la **propiedad SHORTFILENAMES** hace que se utilicen nombres de archivo cortos para los nombres de los archivos de destino, en lugar de nombres de archivo largos. No afecta a los nombres de archivo que busca el instalador en el origen.

## <a name="default-value"></a>Valor predeterminado

El instalador usa nombres largos si no se establece la propiedad **SHORTFILENAMES** y el volumen de destino admite nombres largos. El instalador usa nombres cortos si el volumen de destino no admite nombres largos.

## <a name="remarks"></a>Observaciones

Cuando se establece la propiedad **SHORTFILENAMES,** el instalador crea carpetas e instala archivos mediante nombres de archivo cortos de cualquier par largo corto que aparezca en la tabla Archivo o en la \| tabla [Directorio](directory-table.md). [](file-table.md)

Las aplicaciones pueden usar [**la función GetShortPathName para**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) recuperar el formato de ruta de acceso corta de una ruta de acceso de archivo especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
