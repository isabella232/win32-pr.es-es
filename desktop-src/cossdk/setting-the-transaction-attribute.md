---
description: Puede establecer los atributos de transacción manualmente mediante la herramienta administrativa Servicios de componentes o puede Agregar compatibilidad mediante programación para las transacciones al escribir el componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Establecer el atributo de transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153384"
---
# <a name="setting-the-transaction-attribute"></a>Establecer el atributo de transacción

Puede establecer los atributos de transacción manualmente mediante la herramienta administrativa Servicios de componentes o puede Agregar compatibilidad mediante programación para las transacciones al escribir el componente.

Para más información sobre los valores de atributo de transacción, consulte [configuración de transacciones](configuring-transactions.md).

**Para establecer el valor del atributo mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **transacciones** .

3.  En **compatibilidad con transacciones**, seleccione la opción correspondiente al valor que desee. **No se admite** el valor predeterminado de todos los componentes.

4.  Haga clic en **OK**.

Debe repetir este procedimiento para cada componente.

## <a name="to-set-the-attribute-value-programmatically"></a>Para establecer el valor de atributo mediante programación

Los programadores que usan Microsoft Visual Basic pueden establecer el atributo de transacción con **MTSTransactionMode**, una propiedad de módulo de clase para los proyectos dll de ActiveX. Visual Basic asigna la selección al valor de atributo de transacción COM+ equivalente y publica el valor en la biblioteca de tipos del componente.

En la tabla siguiente se asigna cada valor constante **MTSTransactionMode** a su valor de transacción com+ equivalente.



| MTSTransactionMode constante)         | Valor de transacción de COM+             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (valor predeterminado)<br/> | Disabled<br/>                |
| Notransactions<br/>           | No compatible (valor predeterminado)<br/> |
| RequiresTransaction <br/>     | Obligatorio<br/>                |
| UsesTransaction <br/>         | Compatible<br/>               |
| RequiresNewTransaction <br/>  | Se requiere nueva<br/>            |



 

También se puede tener acceso a la propiedad **MTSTransactionMode** mediante programación con la API de la biblioteca de administración de com+.

 

 




