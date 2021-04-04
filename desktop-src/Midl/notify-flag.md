---
title: notify_flag atributo)
description: El atributo \ Notify \_ Flag \ proporciona una notificación que identifica si se llama a una rutina de servidor.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag el atributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076574"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="696d5-104">atributo de marca de notificación \_</span><span class="sxs-lookup"><span data-stu-id="696d5-104">notify\_flag attribute</span></span>

<span data-ttu-id="696d5-105">El atributo **\[ Notify \_ Flag \]** proporciona una notificación que identifica si se llama a una rutina de servidor.</span><span class="sxs-lookup"><span data-stu-id="696d5-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="696d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="696d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="696d5-107">*procedimiento: nombre*</span><span class="sxs-lookup"><span data-stu-id="696d5-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="696d5-108">Nombre del procedimiento remoto con el que \_ está asociado el procedimiento de marca de notificación.</span><span class="sxs-lookup"><span data-stu-id="696d5-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="696d5-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="696d5-109">Remarks</span></span>

<span data-ttu-id="696d5-110">El atributo **\[ Notify \_ Flag \]** es similar en el uso del atributo **\[ Notify \]** .</span><span class="sxs-lookup"><span data-stu-id="696d5-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="696d5-111">El nombre del procedimiento de **\[ \_ marca \] de notificación** es el nombre del procedimiento remoto con el sufijo de la **\_ \_ marca de notificación**.</span><span class="sxs-lookup"><span data-stu-id="696d5-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="696d5-112">El procedimiento **\_ Notify \_ Flag** no requiere ningún parámetro y no devuelve un resultado.</span><span class="sxs-lookup"><span data-stu-id="696d5-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="696d5-113">También se genera un prototipo de este procedimiento en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="696d5-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="696d5-114">Por ejemplo, si el archivo IDL contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="696d5-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="696d5-115">Especifique lo siguiente en ACF para MIDL a fin de generar la llamada a la **\_ \_ marca de notificación** :</span><span class="sxs-lookup"><span data-stu-id="696d5-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="696d5-116">El compilador MIDL generará código auxiliar de servidor que contiene la siguiente llamada al procedimiento de **\_ \_ marca de notificación** :</span><span class="sxs-lookup"><span data-stu-id="696d5-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="696d5-117">El archivo de encabezado contendrá un prototipo:</span><span class="sxs-lookup"><span data-stu-id="696d5-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="696d5-118">**\_ MIDL \_ NotifyFlag** es **true** si se llama a la rutina de servidor.</span><span class="sxs-lookup"><span data-stu-id="696d5-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="696d5-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="696d5-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="696d5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="696d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="696d5-121">**notificar a**</span><span class="sxs-lookup"><span data-stu-id="696d5-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




