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
# <a name="using-an-object-constructor-string-to-construct-a-component"></a><span data-ttu-id="3e00a-103">Usar una cadena de constructor de objeto para construir un componente</span><span class="sxs-lookup"><span data-stu-id="3e00a-103">Using an Object Constructor String to Construct a Component</span></span>

<span data-ttu-id="3e00a-104">En el ejemplo siguiente se muestra cómo recuperar y usar mediante programación una cadena de constructor de objeto cuando se crea una instancia de un componente.</span><span class="sxs-lookup"><span data-stu-id="3e00a-104">The following example illustrates how to programmatically retrieve and use an object constructor string when a component is instantiated.</span></span> <span data-ttu-id="3e00a-105">Muestra una implementación de la interfaz [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) que recupera una cadena de constructor de objeto.</span><span class="sxs-lookup"><span data-stu-id="3e00a-105">It shows an implementation of the [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) interface that retrieves an object constructor string.</span></span> <span data-ttu-id="3e00a-106">A continuación, se puede analizar la cadena para establecer los valores iniciales o influir en el comportamiento del componente.</span><span class="sxs-lookup"><span data-stu-id="3e00a-106">The string can then be parsed to set initial values or influence the behavior of the component.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3e00a-107">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3e00a-107">Visual Basic</span></span>


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="3e00a-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e00a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e00a-109">Conceptos de las cadenas del constructor de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="3e00a-109">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="3e00a-110">Especificar una cadena de constructor de objeto para un componente</span><span class="sxs-lookup"><span data-stu-id="3e00a-110">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



