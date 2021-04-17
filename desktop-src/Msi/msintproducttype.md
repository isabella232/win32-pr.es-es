---
description: El instalador establece la propiedad MsiNTProductType para los sistemas operativos Windows NT, Windows 2000 y versiones posteriores.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propiedad MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671202"
---
# <a name="msintproducttype-property"></a>Propiedad MsiNTProductType

El instalador establece la propiedad **MsiNTProductType** para los sistemas operativos Windows NT, Windows 2000 y versiones posteriores. Esta propiedad indica el tipo de producto de Windows.

En el caso de los sistemas operativos Windows 2000 y versiones posteriores, el instalador establece los siguientes valores. Tenga en cuenta que los valores son los mismos que los del campo **wProductType** de la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .



| Value | Significado                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional y versiones posteriores      |
| 2     | Controlador de dominio de Windows 2000 y versiones posteriores |
| 3     | Windows 2000 Server y versiones posteriores            |



 

En el caso de sistemas operativos anteriores a Windows 2000, el instalador establece los siguientes valores.



| Value | Significado                      |
|-------|------------------------------|
| 1     | Estación de trabajo Windows NT       |
| 2     | Controlador de dominio de Windows NT |
| 3     | Windows NT Server            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
