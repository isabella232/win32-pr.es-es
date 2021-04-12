---
title: Propiedad AutoPopupMenu
description: Propiedad AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357486"
---
# <a name="autopopupmenu-property"></a>Propiedad AutoPopupMenu

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si al hacer clic con el botón secundario en el carácter o en el icono de la barra de tareas se muestra automáticamente el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. ***Caracteres * * * * ("*** CharacterID * * *"). AutoPopupMenu* *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que especifica si el servidor muestra automáticamente el menú emergente del carácter al hacer clic con el botón secundario. **True** (valor predeterminado) muestra el menú al hacer clic con el botón secundario. <br/> **False** No muestra el menú al hacer clic con el botón secundario.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al establecer esta propiedad en **false**, puede crear su propio comportamiento de control de menús. Para mostrar el menú después de establecer esta propiedad en **false**, use el método [**ShowPopupMenu**](showpopupmenu-method.md) .

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Método ShowPopupMenu**](showpopupmenu-method.md)


 

 





