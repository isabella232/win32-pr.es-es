---
title: Método ShowPopupMenu
description: Método ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704583"
---
# <a name="showpopupmenu-method"></a>Método ShowPopupMenu

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Muestra el menú emergente del carácter situado en la ubicación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*directivas. ***Caracteres ("*** CharacterID ***"). ShowPopupMenu*** x, y*



| Parte | Descripción                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Obligatorio. Valor entero que indica la coordenada de pantalla horizontal (*x*) para mostrar el menú. Estas coordenadas se deben especificar en píxeles. |
| *y*  | Obligatorio. Valor entero que indica la coordenada de pantalla vertical (*y*) para mostrar el menú. Estas coordenadas se deben especificar en píxeles.   |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El agente muestra automáticamente el menú emergente del carácter cuando el usuario hace clic con el botón secundario en el carácter. Si establece [**AutoPopupMenu**](autopopupmenu-property.md) en **false**, puede usar este método para mostrar el menú.

El menú permanecerá en pantalla hasta que el usuario seleccione un comando o muestre otro menú. Solo se puede mostrar un menú emergente a la vez; por lo tanto, las llamadas a este método cancelarán (quitará) el menú anterior.

Solo se debe llamar a este método cuando la aplicación cliente es el cliente activo del carácter; en caso contrario, se produce un error. Para determinar si este método se ha ejecutado correctamente, puede llamarlo como una función y devolverá un valor booleano que indica si el método se ha ejecutado correctamente.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Consulte también

[**Propiedad AutoPopupMenu**](autopopupmenu-property.md)


 

 




