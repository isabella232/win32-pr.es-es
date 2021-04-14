---
description: Usar una cadena de constructor de objeto para construir un componente
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Usar una cadena de constructor de objeto para construir un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496312"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>Usar una cadena de constructor de objeto para construir un componente

En el ejemplo siguiente se muestra cómo recuperar y usar mediante programación una cadena de constructor de objeto cuando se crea una instancia de un componente. Muestra una implementación de la interfaz [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) que recupera una cadena de constructor de objeto. A continuación, se puede analizar la cadena para establecer los valores iniciales o influir en el comportamiento del componente.

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de las cadenas del constructor de objetos COM+](com--object-constructor-strings-concepts.md)
</dt> <dt>

[Especificar una cadena de constructor de objeto para un componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



