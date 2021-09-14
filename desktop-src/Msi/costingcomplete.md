---
description: La propiedad CostingComplete indica si el instalador ha completado el costo del espacio en disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propiedad CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158751"
---
# <a name="costingcomplete-property"></a>Propiedad CostingComplete

La **propiedad CostingComplete** indica si el instalador ha completado el costo del espacio en disco. Esta propiedad se puede usar para crear un cuadro de diálogo desencadenado si no se ha completado el costo. La propiedad se establece dinámicamente durante el costo del espacio en disco y se establece en 1 en cuanto se completa el costo. Esta propiedad se inicializa en 0 mediante la [acción CostFinalize](costfinalize-action.md).

## <a name="remarks"></a>Observaciones

Para obtener un ejemplo de cómo crear un elemento "Espere . . . " cuadro de diálogo que aparece durante el costo de espacio en disco, vea la sección Creación de un condicional ["Espere . . ." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




