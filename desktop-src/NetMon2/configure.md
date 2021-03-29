---
description: Configura el experto en el archivo DLL de expertos.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurar la función de devolución de llamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667120"
---
# <a name="configure-callback-function"></a><span data-ttu-id="c9974-103">Configuración de la función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="c9974-103">Configure callback function</span></span>

<span data-ttu-id="c9974-104">La función **configurar** configura el experto en el archivo dll de expertos.</span><span class="sxs-lookup"><span data-stu-id="c9974-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="c9974-105">El experto debe implementar la función de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="c9974-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="c9974-106">Cuando se recibe la llamada de función, el experto muestra un cuadro de diálogo que permite al usuario cambiar cualquier elemento configurable.</span><span class="sxs-lookup"><span data-stu-id="c9974-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9974-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9974-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="c9974-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9974-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9974-109">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9974-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9974-110">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="c9974-110">Unique expert identifier.</span></span>

<span data-ttu-id="c9974-111">El identificador único se pasa de nuevo en todas las funciones de Monitor de red específicas del experto.</span><span class="sxs-lookup"><span data-stu-id="c9974-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="c9974-112">Tenga en cuenta que el identificador no puede ser la misma clave de experto que el que se pasa a la función [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="c9974-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="c9974-113">No almacene la clave experta de la llamada a **Configure** .</span><span class="sxs-lookup"><span data-stu-id="c9974-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="c9974-114">*ppConfig* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c9974-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9974-115">Un puntero a un puntero a una estructura [**EXPERTCONFIG**](expertconfig.md) en la entrada.</span><span class="sxs-lookup"><span data-stu-id="c9974-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="c9974-116">Después de una salida correcta, la estructura [**EXPERTCONFIG**](expertconfig.md) a la que se hace referencia contiene los nuevos datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="c9974-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="c9974-117">*pExpertStartupInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9974-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9974-118">Puntero al elemento de captura con el foco cuando se inicia el experto.</span><span class="sxs-lookup"><span data-stu-id="c9974-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="c9974-119">*StartupFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9974-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9974-120">Marcas que indican cómo el experto debe usar el parámetro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="c9974-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="c9974-121">La única marca definida es **el \_ indicador de inicio experto que \_ \_ usa datos de \_ Inicio sobre los \_ \_ \_ \_ datos de configuración**.</span><span class="sxs-lookup"><span data-stu-id="c9974-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="c9974-122">La marca indica que el experto usará el parámetro *pExpertStartupInfo* en lugar del parámetro *ppConfig* que se pasó.</span><span class="sxs-lookup"><span data-stu-id="c9974-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="c9974-123">Normalmente, la marca se establece cuando se inicia el experto desde un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="c9974-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="c9974-124">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9974-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9974-125">Identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="c9974-125">A handle to the parent window.</span></span> <span data-ttu-id="c9974-126">Use el identificador para abrir un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c9974-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9974-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9974-127">Return value</span></span>

<span data-ttu-id="c9974-128">Si la función es correcta (es decir, si existe una configuración actual), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="c9974-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="c9974-129">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="c9974-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9974-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9974-130">Remarks</span></span>

<span data-ttu-id="c9974-131">Monitor de red llama a la función **Configure** con la configuración actual del experto, si existe una.</span><span class="sxs-lookup"><span data-stu-id="c9974-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="c9974-132">El experto muestra un cuadro de diálogo, con el que puede cambiar cualquier elemento configurable.</span><span class="sxs-lookup"><span data-stu-id="c9974-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="c9974-133">Cuando se pasa *ppConfig* y monitor de red no tiene una configuración almacenada para el experto especificado, el valor del parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c9974-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="c9974-134">En este caso, la función **Configure** presupone valores predeterminados codificados de forma rígida (o usa la información de inicio) para abrir el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c9974-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="c9974-135">Los datos de configuración también pueden ser **null** cuando se devuelve la función **Configure** y se pasó un **valor null** .</span><span class="sxs-lookup"><span data-stu-id="c9974-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="c9974-136">Esta situación se produce cuando Monitor de red no tiene un valor predeterminado almacenado y el usuario presiona **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="c9974-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="c9974-137">El principio de la estructura de datos [**EXPERTCONFIG**](expertconfig.md) incluye una sección privada que almacena la información sobre el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="c9974-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="c9974-138">El tamaño de la estructura **EXPERTCONFIG** debe incluir la longitud de **DWORD** reservada que aparece al principio de la estructura.</span><span class="sxs-lookup"><span data-stu-id="c9974-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="c9974-139">Por ejemplo, si los datos de configuración requieren 20 bytes de espacio de almacenamiento, asigne 24 bytes para almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="c9974-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="c9974-140">Si *ppConfig* es **null**, la función **Configure** llama a la función [**ExpertAllocMemory**](expertallocmemory.md) para asignar una nueva configuración que tenga el tamaño correcto.</span><span class="sxs-lookup"><span data-stu-id="c9974-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="c9974-141">Si el búfer no es suficiente para contener los datos del experto, el experto debe llamar a la función [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="c9974-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9974-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9974-142">Requirements</span></span>



| <span data-ttu-id="c9974-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9974-143">Requirement</span></span> | <span data-ttu-id="c9974-144">Value</span><span class="sxs-lookup"><span data-stu-id="c9974-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9974-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9974-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c9974-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c9974-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c9974-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9974-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c9974-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9974-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9974-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9974-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9974-150"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9974-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




