---
description: La función CreateHandoffTable crea una tabla de entrega que incluye la información del conjunto de entrega almacenada en el archivo INI del analizador.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Función CreateHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667119"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="ef543-103">CreateHandoffTable función)</span><span class="sxs-lookup"><span data-stu-id="ef543-103">CreateHandoffTable function</span></span>

<span data-ttu-id="ef543-104">La función **CreateHandoffTable** crea una [*tabla de entrega*](h.md) que incluye la información del conjunto de entrega almacenada en el archivo ini del analizador.</span><span class="sxs-lookup"><span data-stu-id="ef543-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef543-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef543-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="ef543-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef543-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef543-107">*secName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef543-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef543-108">Cadena que indica la sección del archivo INI donde se encuentra la información del conjunto de entrega.</span><span class="sxs-lookup"><span data-stu-id="ef543-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="ef543-109">*inifile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef543-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef543-110">Cadena que incluye el nombre del archivo INI del analizador.</span><span class="sxs-lookup"><span data-stu-id="ef543-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="ef543-111">*hTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ef543-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef543-112">Identificador de una estructura **HANDOFFTABLE** creada y mantenida por monitor de red.</span><span class="sxs-lookup"><span data-stu-id="ef543-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ef543-113">*nMaxProtocolEntries* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef543-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef543-114">Número que especifica el número máximo de entradas que puede procesar la tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="ef543-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="ef543-115">*base* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ef543-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef543-116">Base numérica de los números de conjunto de entrega almacenados en el archivo INI.</span><span class="sxs-lookup"><span data-stu-id="ef543-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef543-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef543-117">Return value</span></span>

<span data-ttu-id="ef543-118">Si la función se realiza correctamente, el valor devuelto es el número de entradas de la tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="ef543-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="ef543-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="ef543-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef543-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef543-120">Remarks</span></span>

<span data-ttu-id="ef543-121">La tabla de entrega creada por Monitor de red se basa en la información proporcionada en el INI del analizador.</span><span class="sxs-lookup"><span data-stu-id="ef543-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="ef543-122">A continuación, el identificador devuelto para la tabla de entrega se puede usar para obtener un identificador de uno de los protocolos incluidos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ef543-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="ef543-123">Para obtener un identificador de uno de estos protocolos, llame a [GetProtocolFromTable](getprotocolfromtable.md).</span><span class="sxs-lookup"><span data-stu-id="ef543-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="ef543-124">Tenga en cuenta que la aplicación de analizador nunca accede directamente a la estructura **HANDOFFTABLE** .</span><span class="sxs-lookup"><span data-stu-id="ef543-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="ef543-125">Monitor de red crea y mantiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="ef543-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef543-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef543-126">Requirements</span></span>



| <span data-ttu-id="ef543-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef543-127">Requirement</span></span> | <span data-ttu-id="ef543-128">Value</span><span class="sxs-lookup"><span data-stu-id="ef543-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef543-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef543-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ef543-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef543-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ef543-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef543-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ef543-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef543-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ef543-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef543-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef543-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef543-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ef543-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef543-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef543-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef543-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef543-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef543-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef543-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef543-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef543-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef543-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef543-140">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="ef543-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="ef543-141">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="ef543-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




