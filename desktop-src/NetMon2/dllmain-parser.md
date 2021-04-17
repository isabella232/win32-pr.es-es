---
description: La función de exportación de DllMain para el analizador identifica la existencia del analizador y libera los recursos que utiliza Monitor de red para el analizador. DllMain debe implementarse en todos los archivos dll de analizador.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Función de devolución de llamada del analizador DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667733"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="80bad-104">Función de devolución de llamada del analizador DllMain</span><span class="sxs-lookup"><span data-stu-id="80bad-104">DllMain Parser callback function</span></span>

<span data-ttu-id="80bad-105">La función de exportación de **DllMain** para el analizador identifica la existencia del analizador y libera los recursos que utiliza monitor de red para el analizador.</span><span class="sxs-lookup"><span data-stu-id="80bad-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="80bad-106">**DllMain** debe implementarse en todos los archivos dll de analizador.</span><span class="sxs-lookup"><span data-stu-id="80bad-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80bad-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="80bad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80bad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80bad-109">*hInstance* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80bad-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bad-110">Identificador de una instancia del analizador.</span><span class="sxs-lookup"><span data-stu-id="80bad-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="80bad-111">*Comando* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80bad-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bad-112">Indicador para determinar por qué se llama a la función.</span><span class="sxs-lookup"><span data-stu-id="80bad-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="80bad-113">Para obtener una lista de todas las marcas posibles, vea [DllMain](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="80bad-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="80bad-114">La implementación del analizador debe procesar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="80bad-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="80bad-115">Value</span><span class="sxs-lookup"><span data-stu-id="80bad-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="80bad-116">Significado</span><span class="sxs-lookup"><span data-stu-id="80bad-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="80bad-117"><dt>**\_adjuntar proceso dll \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80bad-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="80bad-118">Cuando se llama a **DllMain** por primera vez, el archivo DLL debe llamar a [CreateProtocol](createprotocol.md) para proporcionar información monitor de red.</span><span class="sxs-lookup"><span data-stu-id="80bad-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="80bad-119"><dt>**desasociación de \_ procesos dll \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80bad-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="80bad-120">Cuando se llama a **DllMain** por última vez, el archivo DLL debe llamar a [DestroyProtocol](destroyprotocol.md) para liberar los recursos que utiliza el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="80bad-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="80bad-121">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="80bad-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="80bad-122">No se utiliza ahora.</span><span class="sxs-lookup"><span data-stu-id="80bad-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80bad-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80bad-123">Return value</span></span>

<span data-ttu-id="80bad-124">El archivo DLL del analizador siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="80bad-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="80bad-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80bad-125">Remarks</span></span>

<span data-ttu-id="80bad-126">El sistema operativo llama a **DllMain** para cargar y descargar el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="80bad-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="80bad-127">Esta función se basa en la función [DllMain](/windows/desktop/Dlls/dllmain) de la biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="80bad-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="80bad-128">También puede usar la implementación de **DllMain** para almacenar una instancia de un analizador para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="80bad-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="80bad-129">Por ejemplo, puede almacenar una instancia de DLL de analizador y, a continuación, utilizarla para una llamada del sistema en el futuro.</span><span class="sxs-lookup"><span data-stu-id="80bad-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="80bad-130">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="80bad-130">For information on</span></span>                                        | <span data-ttu-id="80bad-131">Vea</span><span class="sxs-lookup"><span data-stu-id="80bad-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="80bad-132">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="80bad-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="80bad-133">Analizadores</span><span class="sxs-lookup"><span data-stu-id="80bad-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="80bad-134">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="80bad-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="80bad-135">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="80bad-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="80bad-136">Cómo implementar **DllMain**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="80bad-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="80bad-137">Implementar DllMain</span><span class="sxs-lookup"><span data-stu-id="80bad-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="80bad-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80bad-138">Requirements</span></span>



| <span data-ttu-id="80bad-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="80bad-139">Requirement</span></span> | <span data-ttu-id="80bad-140">Value</span><span class="sxs-lookup"><span data-stu-id="80bad-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="80bad-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80bad-141">Minimum supported client</span></span><br/> | <span data-ttu-id="80bad-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="80bad-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="80bad-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80bad-143">Minimum supported server</span></span><br/> | <span data-ttu-id="80bad-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80bad-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="80bad-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80bad-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="80bad-146"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="80bad-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80bad-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="80bad-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bad-148">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="80bad-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="80bad-149">DestroyProtocol</span><span class="sxs-lookup"><span data-stu-id="80bad-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="80bad-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="80bad-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

