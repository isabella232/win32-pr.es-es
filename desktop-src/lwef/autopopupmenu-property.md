---
title: Propiedad AutoPopupMenu
description: Propiedad AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170233"
---
# <a name="autopopupmenu-property"></a>Propiedad AutoPopupMenu

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si al hacer clic con el botón derecho en el carácter o en el icono de la barra de tareas se muestra automáticamente el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters*("CharacterID***_"). AutoPopupMenu_ *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el servidor muestra automáticamente el menú emergente del carácter al hacer clic con el botón derecho. **True** (valor predeterminado) Muestra el menú al hacer clic con el botón derecho. <br/> **False** No muestra el menú al hacer clic con el botón derecho.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al establecer esta propiedad en **False**, puede crear su propio comportamiento de control de menús. Para mostrar el menú después de establecer esta propiedad en **False,** use el [**método ShowPopupMenu.**](showpopupmenu-method.md)

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Método ShowPopupMenu**](showpopupmenu-method.md)


 

 





