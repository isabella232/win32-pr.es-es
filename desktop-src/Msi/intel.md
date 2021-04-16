---
description: La propiedad Intel se establece mediante el Windows Installer en el nivel de procesador numérico cuando se ejecuta en un procesador Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Propiedad Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690572"
---
# <a name="intel-property"></a>Propiedad Intel

La propiedad **Intel** se establece mediante el Windows Installer en el nivel de procesador numérico cuando se ejecuta en un procesador Intel. Los valores son los mismos que el campo *wProcessorLevel* de la estructura de [**\_ información del sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) . Cuando se ejecuta en un procesador x64, el Windows Installer establece la propiedad **Intel** para que refleje el procesador x86 emulado por el equipo x64, tal y como lo indica el sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
