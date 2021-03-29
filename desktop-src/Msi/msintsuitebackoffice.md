---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteBackOffice en 1 si los componentes de Microsoft BackOffice están instalados.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Propiedad MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653916"
---
# <a name="msintsuitebackoffice-property"></a>Propiedad MsiNTSuiteBackOffice

En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteBackOffice** en 1 si los componentes de Microsoft BackOffice están instalados. El instalador establece esta propiedad en 1 solo si la \_ marca de BackOffice del conjunto de versión \_ se establece en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
