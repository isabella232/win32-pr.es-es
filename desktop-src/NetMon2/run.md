---
description: El experto debe implementar la función de ejecución. Monitor de red llama a la función Run para iniciar el experto en el archivo DLL de expertos.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Ejecutar función de devolución de llamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908115"
---
# <a name="run-callback-function"></a><span data-ttu-id="5290d-104">Ejecutar función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="5290d-104">Run callback function</span></span>

<span data-ttu-id="5290d-105">El experto debe implementar la función de **ejecución** .</span><span class="sxs-lookup"><span data-stu-id="5290d-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="5290d-106">Monitor de red llama a la función **Run** para iniciar el experto en el archivo dll de expertos.</span><span class="sxs-lookup"><span data-stu-id="5290d-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5290d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5290d-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="5290d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5290d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5290d-109">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5290d-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5290d-110">Identificador único del experto que se pasa de nuevo a todas las funciones de Monitor de red específicas del experto.</span><span class="sxs-lookup"><span data-stu-id="5290d-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="5290d-111">El identificador *hExpertKey* puede pasar una clave experta que sea diferente de la clave experta que pasa la función [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="5290d-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="5290d-112">*pConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5290d-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5290d-113">Puntero a la configuración existente.</span><span class="sxs-lookup"><span data-stu-id="5290d-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="5290d-114">El parámetro *pConfig* puede ser **null** , lo que significa que el experto puede ejecutarse con valores predeterminados codificados de forma rígida o con información de inicio a la que hace referencia el parámetro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="5290d-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="5290d-115">*pExpertStartupInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5290d-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5290d-116">Puntero al elemento de captura que tiene el foco cuando se inicia el experto.</span><span class="sxs-lookup"><span data-stu-id="5290d-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="5290d-117">*StartupFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5290d-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5290d-118">Indicador de cómo el experto debe usar el parámetro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="5290d-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="5290d-119">La única marca definida es:</span><span class="sxs-lookup"><span data-stu-id="5290d-119">The only flag defined is:</span></span>



| <span data-ttu-id="5290d-120">Value</span><span class="sxs-lookup"><span data-stu-id="5290d-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="5290d-121">Significado</span><span class="sxs-lookup"><span data-stu-id="5290d-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="5290d-122"><dt>**marca de inicio de experto \_ \_ \_ use \_ datos de inicio \_ \_ sobre \_ datos de configuración \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="5290d-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="5290d-123">Esta marca indica que el experto usa el parámetro *pExpertStartupInfo* y no usa el parámetro *pConfig* .</span><span class="sxs-lookup"><span data-stu-id="5290d-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="5290d-124">Normalmente, puede establecer esta marca cuando el experto puede empezar con un clic con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="5290d-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="5290d-125">Si no se establece la marca, pueden producirse las dos cosas siguientes: el experto no se inicia con un clic con el botón derecho, o el experto comienza con un clic con el botón secundario y, a continuación, el usuario lo configura.</span><span class="sxs-lookup"><span data-stu-id="5290d-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5290d-126">*hWndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5290d-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5290d-127">Parámetro *hWnd* del elemento primario (normalmente la interfaz de usuario monitor de red).</span><span class="sxs-lookup"><span data-stu-id="5290d-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5290d-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5290d-128">Return value</span></span>

<span data-ttu-id="5290d-129">Si la función es correcta (es decir, si se inicia el experto), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="5290d-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="5290d-130">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="5290d-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5290d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5290d-131">Remarks</span></span>

<span data-ttu-id="5290d-132">Al ejecutar, el experto crea un bucle a través de los fotogramas del archivo de captura y genera un informe o los eventos que muestran problemas.</span><span class="sxs-lookup"><span data-stu-id="5290d-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="5290d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5290d-133">Requirements</span></span>



| <span data-ttu-id="5290d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5290d-134">Requirement</span></span> | <span data-ttu-id="5290d-135">Value</span><span class="sxs-lookup"><span data-stu-id="5290d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5290d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5290d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5290d-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5290d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5290d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5290d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5290d-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5290d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5290d-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5290d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5290d-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5290d-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




