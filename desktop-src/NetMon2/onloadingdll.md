---
description: Carga el archivo DLL del monitor.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Función OnLoadingDLL (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677455"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="6c3cc-103">OnLoadingDLL función)</span><span class="sxs-lookup"><span data-stu-id="6c3cc-103">OnLoadingDLL function</span></span>

<span data-ttu-id="6c3cc-104">La función **OnLoadingDLL** carga el archivo dll de supervisión.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c3cc-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="6c3cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c3cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3cc-107">*hFilterBlob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c3cc-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3cc-108">Un BLOB que utiliza el MCSVC para que coincida con un monitor con NIC disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="6c3cc-109">Este parámetro siempre contiene una solicitud de una interfaz [IRTC](irtc.md) , por lo que la mayoría de los monitores no necesitan agregar entradas al BLOB.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="6c3cc-110">Sin embargo, un monitor personalizado puede Agregar criterios de filtro adicionales (por ejemplo, que el tipo MAC debe ser Ethernet).</span><span class="sxs-lookup"><span data-stu-id="6c3cc-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="6c3cc-111">*pCreateFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c3cc-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3cc-112">Marcas que indican cómo el MCSVC controla la creación de un monitor.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="6c3cc-113">Este parámetro debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="6c3cc-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="6c3cc-114">Value</span><span class="sxs-lookup"><span data-stu-id="6c3cc-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="6c3cc-115">Significado</span><span class="sxs-lookup"><span data-stu-id="6c3cc-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="6c3cc-116"><dt>**MCS \_ crear \_ uno \_ por \_ tarjeta de**</dt></span><span class="sxs-lookup"><span data-stu-id="6c3cc-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="6c3cc-117">MCSVC garantiza que solo existe una instancia de este monitor para cada NIC.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="6c3cc-118">Solo se puede crear una segunda instancia si se destruye la primera.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="6c3cc-119"><dt>**\_crear \_ configuraciones de MCS \_ de forma \_ predeterminada**</dt></span><span class="sxs-lookup"><span data-stu-id="6c3cc-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="6c3cc-120">Si el monitor tiene una configuración interna predeterminada, MCSVC no requiere que el usuario configure el monitor antes de crear la instancia.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="6c3cc-121">*ppDefaultName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c3cc-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3cc-122">Un puntero a un puntero a la dirección del nombre predeterminado del monitor.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="6c3cc-123">MCSVC usa el nombre predeterminado al crear instancias del monitor.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="6c3cc-124">Por ejemplo, si el nombre predeterminado devuelto es "router monitor", la primera instancia del monitor sería "router monitor 1", la segunda sería "RouterMonitor2, etc.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="6c3cc-125">Si se devuelve **null** , MCSVC utiliza el nombre del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="6c3cc-126">*ppDescription* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c3cc-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3cc-127">Un puntero a un puntero a la dirección de la descripción del monitor.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="6c3cc-128">La descripción se pasa a la herramienta supervisar control, que usa la descripción para indicar al usuario que el monitor existe.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="6c3cc-129">Este parámetro puede devolver **null**.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c3cc-130">*ppDefaultScript* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c3cc-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3cc-131">Un puntero a un puntero a la dirección del script de formulario HTML predeterminado que se usa para configurar el monitor.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="6c3cc-132">Aunque las instancias del monitor pueden modificar su propio script, la mayoría de los monitores simplemente cargan su script una vez, desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="6c3cc-133">El valor de *ppDefaultScript* puede ser **null**; sin embargo, el monitor no se puede configurar externamente o debe proporcionar un script más adelante.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="6c3cc-134">Es más eficaz proporcionar aquí un script predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="6c3cc-135">*ppDefaultConfig* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c3cc-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3cc-136">La dirección de la cadena predeterminada que se usa para configurar el monitor cuando se crea.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="6c3cc-137">Este parámetro se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3cc-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c3cc-138">Return value</span></span>

<span data-ttu-id="6c3cc-139">Si la función es correcta, el valor devuelto es S \_ OK; que es igual que NoError.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="6c3cc-140">Si la función no se realiza correctamente, MCSVC omite el monitor especificado de todas sus listas; después de, no se puede crear ningún monitor de este tipo.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3cc-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c3cc-141">Remarks</span></span>

<span data-ttu-id="6c3cc-142">El MCSVC llama a la función **OnLoadingDLL** una vez, la primera vez que carga el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="6c3cc-143">A continuación, el archivo DLL proporciona los valores predeterminados que usará el MCSVC al crear una instancia de un monitor.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="6c3cc-144">El monitor debe asignar toda la memoria necesaria para las cadenas que se devuelven a MCSVC.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="6c3cc-145">En la devolución, el MCSVC realiza copias de todas las cadenas y no intenta liberar las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="6c3cc-146">El monitor debe usar las funciones auxiliares de BLOB para modificar el BLOB de filtro.</span><span class="sxs-lookup"><span data-stu-id="6c3cc-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3cc-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c3cc-147">Requirements</span></span>



| <span data-ttu-id="6c3cc-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3cc-148">Requirement</span></span> | <span data-ttu-id="6c3cc-149">Value</span><span class="sxs-lookup"><span data-stu-id="6c3cc-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3cc-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c3cc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3cc-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c3cc-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6c3cc-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c3cc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3cc-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c3cc-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c3cc-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c3cc-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3cc-155"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3cc-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




