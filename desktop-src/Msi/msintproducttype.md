---
description: El instalador establece la propiedad MsiNTProductType para Windows NT, Windows 2000 y sistemas operativos posteriores.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propiedad MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074365"
---
# <a name="msintproducttype-property"></a>Propiedad MsiNTProductType

El instalador establece la **propiedad MsiNTProductType** para Windows NT, Windows 2000 y sistemas operativos posteriores. Esta propiedad indica el tipo Windows producto.

Para Windows 2000 y sistemas operativos posteriores, el instalador establece los valores siguientes. Tenga en cuenta que los valores son los mismos que los del **campo wProductType** de la [**estructura OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)



| Value | Significado                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional y versiones posteriores      |
| 2     | Windows controlador de dominio 2000 y versiones posteriores |
| 3     | Windows 2000 Server y versiones posteriores            |



 

Para los sistemas operativos anteriores a Windows 2000, el instalador establece los valores siguientes.



| Value | Significado                      |
|-------|------------------------------|
| 1     | Windows Estación de trabajo NT       |
| 2     | Windows Controlador de dominio NT |
| 3     | Windows Servidor NT            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
