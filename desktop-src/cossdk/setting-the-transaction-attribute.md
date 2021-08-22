---
description: Puede establecer los atributos de transacción manualmente mediante la herramienta administrativa Servicios de componentes, o bien puede agregar compatibilidad mediante programación para las transacciones al escribir el componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Establecer el atributo de transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6310d2544090d4b551a93782b4756b3d89f2d6d365dfc09aec4658d5d3e1b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546222"
---
# <a name="setting-the-transaction-attribute"></a>Establecer el atributo de transacción

Puede establecer los atributos de transacción manualmente mediante la herramienta administrativa Servicios de componentes, o bien puede agregar compatibilidad mediante programación para las transacciones al escribir el componente.

Para obtener más información sobre los valores de atributo de transacción, [vea Configuring Transactions](configuring-transactions.md).

**Para establecer el valor del atributo mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón derecho en el componente que desea configurar y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo Propiedades del componente, haga clic **en la pestaña** Transacciones .

3.  En **Compatibilidad con transacciones,** seleccione la opción para el valor que desee. El valor predeterminado de todos los componentes es **No se admite**.

4.  Haga clic en **Aceptar**.

Debe repetir este procedimiento para cada componente.

## <a name="to-set-the-attribute-value-programmatically"></a>Para establecer el valor del atributo mediante programación

Los programadores que usan Microsoft Visual Basic pueden establecer el atributo de transacción con **MTSTransactionMode**, una propiedad de módulo de clase para ActiveX dll. Visual Basic asigna la selección al valor de atributo de transacción COM+ equivalente y publica el valor en la biblioteca de tipos del componente.

En la tabla siguiente se asigna cada valor constante **MTSTransactionMode** a su valor de transacción COM+ equivalente.



| Constante MTSTransactionMode         | Valor de transacción COM+             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (valor predeterminado)<br/> | Disabled<br/>                |
| NoTransactions<br/>           | No compatible (valor predeterminado)<br/> |
| RequiresTransaction <br/>     | Requerido<br/>                |
| UsesTransaction <br/>         | Compatible<br/>               |
| RequiresNewTransaction <br/>  | Se requiere nueva<br/>            |



 

También se puede acceder a la propiedad **MTSTransactionMode** mediante programación mediante la API de biblioteca de administración de COM+.

 

 




