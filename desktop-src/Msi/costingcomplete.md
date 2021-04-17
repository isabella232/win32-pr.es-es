---
description: La propiedad CostingComplete indica si el instalador ha completado el costo de espacio en disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propiedad CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653506"
---
# <a name="costingcomplete-property"></a>Propiedad CostingComplete

La propiedad **CostingComplete** indica si el instalador ha completado el costo de espacio en disco. Esta propiedad se puede usar para crear un cuadro de diálogo desencadenado si no se ha completado el costo. La propiedad se establece dinámicamente durante el costo del espacio en disco y se establece en 1 en cuanto se completa el costo. La [acción CostFinalize](costfinalize-action.md)inicializa esta propiedad en 0.

## <a name="remarks"></a>Observaciones

Para obtener un ejemplo de cómo crear un "espere. . . "cuadro de diálogo que aparece durante el costo de espacio en disco, consulte la sección [creación de una instrucción condicional" espere.... " Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




