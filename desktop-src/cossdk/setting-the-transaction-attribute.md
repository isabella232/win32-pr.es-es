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
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="08165-103">Establecer el atributo de transacción</span><span class="sxs-lookup"><span data-stu-id="08165-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="08165-104">Puede establecer los atributos de transacción manualmente mediante la herramienta administrativa Servicios de componentes o puede Agregar compatibilidad mediante programación para las transacciones al escribir el componente.</span><span class="sxs-lookup"><span data-stu-id="08165-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="08165-105">Para más información sobre los valores de atributo de transacción, consulte [configuración de transacciones](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="08165-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="08165-106">**Para establecer el valor del atributo mediante la herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="08165-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="08165-107">En el árbol de consola, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="08165-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="08165-108">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **transacciones** .</span><span class="sxs-lookup"><span data-stu-id="08165-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="08165-109">En **compatibilidad con transacciones**, seleccione la opción correspondiente al valor que desee.</span><span class="sxs-lookup"><span data-stu-id="08165-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="08165-110">**No se admite** el valor predeterminado de todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="08165-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="08165-111">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="08165-111">Click **OK**.</span></span>

<span data-ttu-id="08165-112">Debe repetir este procedimiento para cada componente.</span><span class="sxs-lookup"><span data-stu-id="08165-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="08165-113">Para establecer el valor de atributo mediante programación</span><span class="sxs-lookup"><span data-stu-id="08165-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="08165-114">Los programadores que usan Microsoft Visual Basic pueden establecer el atributo de transacción con **MTSTransactionMode**, una propiedad de módulo de clase para los proyectos dll de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="08165-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="08165-115">Visual Basic asigna la selección al valor de atributo de transacción COM+ equivalente y publica el valor en la biblioteca de tipos del componente.</span><span class="sxs-lookup"><span data-stu-id="08165-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="08165-116">En la tabla siguiente se asigna cada valor constante **MTSTransactionMode** a su valor de transacción com+ equivalente.</span><span class="sxs-lookup"><span data-stu-id="08165-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="08165-117">MTSTransactionMode constante)</span><span class="sxs-lookup"><span data-stu-id="08165-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="08165-118">Valor de transacción de COM+</span><span class="sxs-lookup"><span data-stu-id="08165-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="08165-119">NotAnMTSObject (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="08165-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="08165-120">Disabled</span><span class="sxs-lookup"><span data-stu-id="08165-120">Disabled</span></span><br/>                |
| <span data-ttu-id="08165-121">Notransactions</span><span class="sxs-lookup"><span data-stu-id="08165-121">NoTransactions</span></span><br/>           | <span data-ttu-id="08165-122">No compatible (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="08165-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="08165-123">RequiresTransaction</span><span class="sxs-lookup"><span data-stu-id="08165-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="08165-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="08165-124">Required</span></span><br/>                |
| <span data-ttu-id="08165-125">UsesTransaction</span><span class="sxs-lookup"><span data-stu-id="08165-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="08165-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="08165-126">Supported</span></span><br/>               |
| <span data-ttu-id="08165-127">RequiresNewTransaction</span><span class="sxs-lookup"><span data-stu-id="08165-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="08165-128">Se requiere nueva</span><span class="sxs-lookup"><span data-stu-id="08165-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="08165-129">También se puede tener acceso a la propiedad **MTSTransactionMode** mediante programación con la API de la biblioteca de administración de com+.</span><span class="sxs-lookup"><span data-stu-id="08165-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




