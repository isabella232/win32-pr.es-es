---
title: ShowPopupMenu (método)
description: ShowPopupMenu (método)
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468781"
---
# <a name="showpopupmenu-method"></a>ShowPopupMenu (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Muestra el menú emergente del carácter en la ubicación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). ShowPopupMenu_ * _x, y_



| Parte | Descripción                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Necesario. Valor entero que indica la coordenada de pantalla horizontal *(x)* para mostrar el menú. Estas coordenadas deben especificarse en píxeles. |
| *y*  | Necesario. Valor entero que indica la coordenada de pantalla vertical (*y*) para mostrar el menú. Estas coordenadas deben especificarse en píxeles.   |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El agente muestra automáticamente el menú emergente del carácter cuando el usuario hace clic con el botón derecho en el carácter. Si establece [**AutoPopupMenu**](autopopupmenu-property.md) en **False,** puede usar este método para mostrar el menú.

El menú permanece mostrado hasta que el usuario selecciona un comando o muestra otro menú. Solo se puede mostrar un menú emergente a la vez; Por lo tanto, las llamadas a este método cancelarán (quitarán) el menú anterior.

Solo se debe llamar a este método cuando la aplicación cliente es el cliente activo del carácter; de lo contrario, se produce un error. Para determinar el éxito de este método, puede llamarlo como una función y devolverá un valor booleano que indica si el método se ha correcto.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Consulte también

[**Propiedad AutoPopupMenu**](autopopupmenu-property.md)


 

 




