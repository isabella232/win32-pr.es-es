---
description: La propiedad Intel se establece mediante el instalador Windows en el nivel de procesador numérico cuando se ejecuta en un procesador Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Propiedad Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072017"
---
# <a name="intel-property"></a>Propiedad Intel

La **propiedad Intel** se establece mediante el instalador Windows en el nivel de procesador numérico cuando se ejecuta en un procesador Intel. Los valores son los mismos que el *campo wProcessorLevel* de la [**estructura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) Cuando se ejecuta en un procesador x64, el instalador de Windows establece la propiedad **Intel** para reflejar el procesador x86 emulado por el equipo x64 tal como lo notifica el sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
