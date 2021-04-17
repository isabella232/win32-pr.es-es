---
description: El instalador establece la propiedad TempFolder en la ruta de acceso completa a la carpeta temporal. No es necesario que los autores establezcan la propiedad TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propiedad TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653371"
---
# <a name="tempfolder-property"></a>Propiedad TempFolder

El instalador establece la propiedad **TempFolder** en la ruta de acceso completa a la carpeta temporal.

No es necesario que los autores establezcan la propiedad **TempFolder** . Windows Installer usa la función [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) para recuperar la ruta de acceso del directorio designado para los archivos temporales y establecer esta propiedad.

## <a name="remarks"></a>Observaciones

Un valor común para esta propiedad es C: \\ temp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
