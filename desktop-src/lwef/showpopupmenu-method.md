---
title: ShowPopupMenu (método)
description: ShowPopupMenu (método)
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cfd080adcf0158a628f019b4d48be5cd10b9c5b47d7a4b71ccd2393ad83ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600995"
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
| *x*  | Obligatorio. Valor entero que indica la coordenada de pantalla horizontal *(x)* para mostrar el menú. Estas coordenadas deben especificarse en píxeles. |
| *y*  | Obligatorio. Valor entero que indica la coordenada de pantalla vertical (*y*) para mostrar el menú. Estas coordenadas deben especificarse en píxeles.   |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

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


 

 




