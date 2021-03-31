---
title: Tipo complejo de LevelType
description: Define un valor de gravedad que determina el nivel de detalle de los eventos que se registran.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- LevelType tipo complejo EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149920"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="4b5d7-104">Tipo complejo de LevelType</span><span class="sxs-lookup"><span data-stu-id="4b5d7-104">LevelType Complex Type</span></span>

<span data-ttu-id="4b5d7-105">Define un valor de gravedad que determina el nivel de detalle de los eventos que se registran.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="4b5d7-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b5d7-106">Attributes</span></span>



| <span data-ttu-id="4b5d7-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b5d7-107">Name</span></span>    | <span data-ttu-id="4b5d7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b5d7-108">Type</span></span>                                                              | <span data-ttu-id="4b5d7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b5d7-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5d7-110">message</span><span class="sxs-lookup"><span data-stu-id="4b5d7-110">message</span></span> | [<span data-ttu-id="4b5d7-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="4b5d7-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="4b5d7-112">El nombre para mostrar adaptado para el nivel.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-112">The localized display name for the level.</span></span> <span data-ttu-id="4b5d7-113">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="4b5d7-114">name</span><span class="sxs-lookup"><span data-stu-id="4b5d7-114">name</span></span>    | <span data-ttu-id="4b5d7-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="4b5d7-115">**QName**</span></span>                                                         | <span data-ttu-id="4b5d7-116">Nombre que se va a asignar a este nivel.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-116">The name to assign to this level.</span></span> <span data-ttu-id="4b5d7-117">Este nombre debe ser único dentro del ámbito del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="4b5d7-118">símbolo</span><span class="sxs-lookup"><span data-stu-id="4b5d7-118">symbol</span></span>  | [<span data-ttu-id="4b5d7-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="4b5d7-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="4b5d7-120">Símbolo que se va a usar para hacer referencia al nivel de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="4b5d7-121">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el nivel en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="4b5d7-122">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="4b5d7-123">value</span><span class="sxs-lookup"><span data-stu-id="4b5d7-123">value</span></span>   | [<span data-ttu-id="4b5d7-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="4b5d7-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="4b5d7-125">Valor de nivel.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-125">The level value.</span></span> <span data-ttu-id="4b5d7-126">Puede especificar valores comprendidos entre 16 y 255.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="4b5d7-127">Para los valores de nivel predefinidos, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="4b5d7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b5d7-128">Remarks</span></span>

<span data-ttu-id="4b5d7-129">A continuación se muestran los valores de nivel predefinidos que puede usar.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="4b5d7-130">Estos valores se definen en el archivo Winmeta.xml que se incluye en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="4b5d7-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b5d7-131">Name</span></span>              | <span data-ttu-id="4b5d7-132">Value</span><span class="sxs-lookup"><span data-stu-id="4b5d7-132">Value</span></span> | <span data-ttu-id="4b5d7-133">Símbolo</span><span class="sxs-lookup"><span data-stu-id="4b5d7-133">Symbol</span></span>                    | <span data-ttu-id="4b5d7-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b5d7-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4b5d7-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="4b5d7-135">win:Critical</span></span>      | <span data-ttu-id="4b5d7-136">1</span><span class="sxs-lookup"><span data-stu-id="4b5d7-136">1</span></span>     | <span data-ttu-id="4b5d7-137">\_nivel \_ crítico de WINEVENT</span><span class="sxs-lookup"><span data-stu-id="4b5d7-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="4b5d7-138">Identifica un evento de salida o finalización anormal.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="4b5d7-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="4b5d7-139">win:Error</span></span>         | <span data-ttu-id="4b5d7-140">2</span><span class="sxs-lookup"><span data-stu-id="4b5d7-140">2</span></span>     | <span data-ttu-id="4b5d7-141">\_error de nivel de WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="4b5d7-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="4b5d7-142">Identifica un evento de error grave.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="4b5d7-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="4b5d7-143">win:Warning</span></span>       | <span data-ttu-id="4b5d7-144">3</span><span class="sxs-lookup"><span data-stu-id="4b5d7-144">3</span></span>     | <span data-ttu-id="4b5d7-145">\_Advertencia de nivel de WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="4b5d7-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="4b5d7-146">Identifica un evento de advertencia, como un error de asignación.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="4b5d7-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="4b5d7-147">win:Informational</span></span> | <span data-ttu-id="4b5d7-148">4</span><span class="sxs-lookup"><span data-stu-id="4b5d7-148">4</span></span>     | <span data-ttu-id="4b5d7-149">\_información de nivel de WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="4b5d7-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="4b5d7-150">Identifica un evento que no es un error, como una entrada o un evento de salida.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="4b5d7-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="4b5d7-151">win:Verbose</span></span>       | <span data-ttu-id="4b5d7-152">5</span><span class="sxs-lookup"><span data-stu-id="4b5d7-152">5</span></span>     | <span data-ttu-id="4b5d7-153">\_nivel \_ detallado de WINEVENT</span><span class="sxs-lookup"><span data-stu-id="4b5d7-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="4b5d7-154">Identifica un evento de seguimiento detallado.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="4b5d7-155">Los números más altos implican también la obtención de niveles inferiores.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="4b5d7-156">Por ejemplo, si especifica Win: Warning, recibirá todos los eventos de advertencia, error y crítico.</span><span class="sxs-lookup"><span data-stu-id="4b5d7-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5d7-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b5d7-157">Requirements</span></span>



| <span data-ttu-id="4b5d7-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b5d7-158">Requirement</span></span> | <span data-ttu-id="4b5d7-159">Value</span><span class="sxs-lookup"><span data-stu-id="4b5d7-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b5d7-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b5d7-160">Minimum supported client</span></span><br/> | <span data-ttu-id="4b5d7-161">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4b5d7-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b5d7-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b5d7-162">Minimum supported server</span></span><br/> | <span data-ttu-id="4b5d7-163">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b5d7-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





