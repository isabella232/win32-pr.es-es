---
description: El instalador establece la propiedad TempFolder en la ruta de acceso completa a la carpeta Temp. Los autores no deben tener que establecer la propiedad TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propiedad TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069614"
---
# <a name="tempfolder-property"></a>Propiedad TempFolder

El instalador establece la **propiedad TempFolder** en la ruta de acceso completa a la carpeta Temp.

Los autores no deben tener que establecer la **propiedad TempFolder.** Windows El instalador usa [**la función GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) para recuperar la ruta de acceso del directorio designado para los archivos temporales y establecer esta propiedad.

## <a name="remarks"></a>Observaciones

Un valor común para esta propiedad es C: \\ Temp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
