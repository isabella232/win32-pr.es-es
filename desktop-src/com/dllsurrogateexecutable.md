---
title: DllSurrogateExecutable
description: Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del registro DllSurrogate. Si no se especifica DllSurrogateExecutable, COM pasa NULL como el valor para el primer parámetro de la función CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valor del registro DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705049"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="0ea79-105">DllSurrogateExecutable</span><span class="sxs-lookup"><span data-stu-id="0ea79-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="0ea79-106">Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del registro [**DllSurrogate**](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="0ea79-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="0ea79-107">Si no se especifica **DllSurrogateExecutable** , com pasa **null** como el valor para el primer parámetro de la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="0ea79-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0ea79-108">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0ea79-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="0ea79-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ea79-109">Remarks</span></span>

<span data-ttu-id="0ea79-110">Este valor es de tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="0ea79-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="0ea79-111">Funciona junto con el valor [**DllSurrogate**](dllsurrogate.md) para evitar cualquier ambigüedad al utilizar la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="0ea79-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="0ea79-112">**DllSurrogate** indica si es necesario usar un suplente personalizado y esta información se pasa como el primer parámetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="0ea79-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="0ea79-113">Dependiendo de la implementación de **CreateProcess**, esta información puede ser ambigua.</span><span class="sxs-lookup"><span data-stu-id="0ea79-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="0ea79-114">Si se especifica **DllSurrogateExecutable** , com pasa el valor como primer parámetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="0ea79-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="0ea79-115">Si no se especifica **DllSurrogateExecutable** , com pasa **null** como el valor para el primer parámetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="0ea79-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ea79-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ea79-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea79-117">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="0ea79-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="0ea79-118">Suplentes DLL</span><span class="sxs-lookup"><span data-stu-id="0ea79-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="0ea79-119">**DllSurrogate**</span><span class="sxs-lookup"><span data-stu-id="0ea79-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="0ea79-120">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="0ea79-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 