---
description: La función SelectNPPBlobFromTable selecciona una NIC de una tabla BLOB de NPP proporcionada.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Función SelectNPPBlobFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275564"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="86988-103">SelectNPPBlobFromTable función)</span><span class="sxs-lookup"><span data-stu-id="86988-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="86988-104">La función **SelectNPPBlobFromTable** selecciona una NIC de una tabla BLOB de NPP proporcionada.</span><span class="sxs-lookup"><span data-stu-id="86988-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="86988-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86988-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="86988-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86988-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86988-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86988-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86988-108">Identificador de la ventana que muestra el cuadro de diálogo **seleccionar una red** .</span><span class="sxs-lookup"><span data-stu-id="86988-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="86988-109">*pBlobTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86988-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86988-110">Puntero a la tabla de BLOBs proporcionada.</span><span class="sxs-lookup"><span data-stu-id="86988-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="86988-111">Monitor de red usa esta tabla para rellenar el cuadro de diálogo **seleccionar una red** .</span><span class="sxs-lookup"><span data-stu-id="86988-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="86988-112">*hBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86988-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86988-113">Identificador del BLOB que representa la NIC seleccionada.</span><span class="sxs-lookup"><span data-stu-id="86988-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86988-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86988-114">Return value</span></span>

<span data-ttu-id="86988-115">Si la función se realiza correctamente y el usuario selecciona una NIC, el valor devuelto es NMERR \_ Success; el BLOB al que apunta *hBlob* se rellena.</span><span class="sxs-lookup"><span data-stu-id="86988-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="86988-116">Si el usuario no selecciona una NIC, el valor devuelto es NMERR \_ no \_ se \_ selecciona NPP.</span><span class="sxs-lookup"><span data-stu-id="86988-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="86988-117">Si la función no es correcta, el valor devuelto es otro valor de NMERR.</span><span class="sxs-lookup"><span data-stu-id="86988-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86988-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86988-118">Remarks</span></span>

<span data-ttu-id="86988-119">Cuando se llama, Monitor de red muestra el cuadro de diálogo **seleccionar una red** , que puede usar para seleccionar una NIC.</span><span class="sxs-lookup"><span data-stu-id="86988-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="86988-120">El BLOB NPP que representa la NIC seleccionada vuelve a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="86988-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="86988-121">Para obtener información sobre las distintas formas en que puede seleccionar NIC, consulte [seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md) .</span><span class="sxs-lookup"><span data-stu-id="86988-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="86988-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86988-122">Requirements</span></span>



| <span data-ttu-id="86988-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="86988-123">Requirement</span></span> | <span data-ttu-id="86988-124">Value</span><span class="sxs-lookup"><span data-stu-id="86988-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86988-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86988-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86988-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="86988-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="86988-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86988-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86988-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86988-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86988-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86988-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86988-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="86988-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="86988-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86988-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="86988-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86988-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="86988-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86988-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86988-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86988-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86988-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="86988-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86988-136">GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="86988-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="86988-137">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="86988-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="86988-138">Entradas de BLOB especiales</span><span class="sxs-lookup"><span data-stu-id="86988-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




