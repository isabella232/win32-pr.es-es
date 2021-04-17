---
title: notificar atributo
description: El atributo \ Notify \ indica al compilador de MIDL que genere una llamada a un procedimiento \ Notify \ en el lado servidor de la aplicación.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notificar al atributo MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532596"
---
# <a name="notify-attribute"></a><span data-ttu-id="c39df-104">notificar atributo</span><span class="sxs-lookup"><span data-stu-id="c39df-104">notify attribute</span></span>

<span data-ttu-id="c39df-105">El atributo **\[ Notify \]** indica al compilador de MIDL que genere una llamada a un procedimiento **\[ Notify \]** en el lado del servidor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c39df-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="c39df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c39df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c39df-107">*procedimiento: nombre*</span><span class="sxs-lookup"><span data-stu-id="c39df-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c39df-108">Nombre del procedimiento remoto con el que se asociará el procedimiento de notificación.</span><span class="sxs-lookup"><span data-stu-id="c39df-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c39df-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c39df-109">Remarks</span></span>

<span data-ttu-id="c39df-110">El procedimiento **\[ Notify \]** llamado como resultado del atributo **\[ Notify \]** está asociado a un procedimiento remoto determinado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="c39df-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="c39df-111">Es similar en concepto a una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c39df-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="c39df-112">El código auxiliar llama al procedimiento **\[ Notify \]** una vez que se han calculado las referencias de todos los argumentos de salida del procedimiento remoto al que está asociado, y se libera cualquier memoria asociada a los parámetros.</span><span class="sxs-lookup"><span data-stu-id="c39df-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="c39df-113">Se llama a la rutina **\[ Notify \]** si se produce un error en una llamada antes de que se ejecute la rutina de servidor.</span><span class="sxs-lookup"><span data-stu-id="c39df-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="c39df-114">Por ejemplo, si se produce un error en un servidor durante la desserialización debido a la recepción de datos incorrectos del cliente, \[ \] se llama a la rutina Notify.</span><span class="sxs-lookup"><span data-stu-id="c39df-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="c39df-115">El atributo **\[ Notify \]** es útil para desarrollar aplicaciones que adquieran recursos en procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="c39df-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="c39df-116">Estos recursos se liberan después en el procedimiento **\[ Notify \]** después de que se calculen las referencias de los parámetros de salida del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="c39df-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="c39df-117">El nombre del procedimiento de **\[ notificación \]** es el nombre del procedimiento remoto con el sufijo de **\_ notificaciones**.</span><span class="sxs-lookup"><span data-stu-id="c39df-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="c39df-118">El procedimiento **\_ Notify** no requiere ningún parámetro y no devuelve un resultado.</span><span class="sxs-lookup"><span data-stu-id="c39df-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="c39df-119">También se genera un prototipo de este procedimiento en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c39df-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="c39df-120">Por ejemplo, si el archivo IDL contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c39df-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="c39df-121">Especifique lo siguiente en ACF para MIDL a fin de generar la llamada a **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="c39df-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="c39df-122">El compilador MIDL generará código auxiliar de servidor que contiene la siguiente llamada al procedimiento **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="c39df-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="c39df-123">El archivo de encabezado contendrá un prototipo:</span><span class="sxs-lookup"><span data-stu-id="c39df-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="c39df-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c39df-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="c39df-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c39df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c39df-126">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="c39df-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 




