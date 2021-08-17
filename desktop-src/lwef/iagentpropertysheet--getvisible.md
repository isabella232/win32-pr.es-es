---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95d1da3d1c0b4e5bf65c2f5f43c67153cc1d6af934e1814735abb12ed8d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692307"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet::GetVisible

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Determina si la hoja de propiedades de Microsoft Agent está visible u oculta.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Dirección de una variable que recibe **True si** la hoja de propiedades está visible y **False** si está oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet::SetVisible**](iagentpropertysheet--setvisible.md)


 

 




