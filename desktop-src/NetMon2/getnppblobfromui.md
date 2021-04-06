---
description: Selecciona una NIC de registro.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Función GetNPPBlobFromUI (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002237"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="55bb8-103">GetNPPBlobFromUI función)</span><span class="sxs-lookup"><span data-stu-id="55bb8-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="55bb8-104">La función **GetNPPBlobFromUI** selecciona una NIC de registro.</span><span class="sxs-lookup"><span data-stu-id="55bb8-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55bb8-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="55bb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55bb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bb8-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55bb8-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55bb8-108">Identificador de una ventana que muestra el cuadro de diálogo **seleccionar una red** .</span><span class="sxs-lookup"><span data-stu-id="55bb8-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="55bb8-109">*hFilterBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55bb8-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55bb8-110">Identificador de un [*BLOB de filtro*](f.md) que se usa para limitar las NIC que se muestran.</span><span class="sxs-lookup"><span data-stu-id="55bb8-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="55bb8-111">*phBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="55bb8-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55bb8-112">Puntero al identificador del BLOB que representa la NIC seleccionada.</span><span class="sxs-lookup"><span data-stu-id="55bb8-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55bb8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55bb8-113">Return value</span></span>

<span data-ttu-id="55bb8-114">Si la función se realiza correctamente (el usuario selecciona una NIC), el valor devuelto es NMERR \_ Success y se rellena el BLOB al que apunta *phBlob* .</span><span class="sxs-lookup"><span data-stu-id="55bb8-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="55bb8-115">Si el usuario no selecciona una NIC, el valor devuelto es **NMERR \_ no \_ se \_ selecciona NPP**.</span><span class="sxs-lookup"><span data-stu-id="55bb8-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="55bb8-116">Si la función no es correcta, el valor devuelto es otro valor de NMERR.</span><span class="sxs-lookup"><span data-stu-id="55bb8-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55bb8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55bb8-117">Remarks</span></span>

<span data-ttu-id="55bb8-118">Cuando se llama, Monitor de red muestra el cuadro de diálogo **seleccionar una red** , que puede usar para seleccionar una NIC.</span><span class="sxs-lookup"><span data-stu-id="55bb8-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="55bb8-119">El BLOB NPP que representa la NIC se devuelve a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="55bb8-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="55bb8-120">Si el BLOB llamado por *hFilterBlob* es un [*BLOB especial*](s.md), el buscador intentará procesarlo.</span><span class="sxs-lookup"><span data-stu-id="55bb8-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="55bb8-121">Un ejemplo sería una llamada que anteriormente devolvía un BLOB especial del NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="55bb8-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="55bb8-122">La aplicación insertó la etiqueta necesaria, el nombre de la máquina \_ .</span><span class="sxs-lookup"><span data-stu-id="55bb8-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="55bb8-123">En esta situación, el buscador pasaría este BLOB al NPP remoto, que luego devolvería una tabla de blobs NPP que representa el equipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="55bb8-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="55bb8-124">Estos blobs NPP remotos aparecerán en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55bb8-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="55bb8-125">El llamador debe llamar a la función [DestroyBlob](destroyblob.md) , que destruye el BLOB devuelto cuando ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="55bb8-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="55bb8-126">Para más información sobre</span><span class="sxs-lookup"><span data-stu-id="55bb8-126">For more information about</span></span> | <span data-ttu-id="55bb8-127">Vea</span><span class="sxs-lookup"><span data-stu-id="55bb8-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="55bb8-128">Tres formas de seleccionar NIC</span><span class="sxs-lookup"><span data-stu-id="55bb8-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="55bb8-129">Seleccionar una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="55bb8-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="55bb8-130">Especificación de un BLOB en filtro</span><span class="sxs-lookup"><span data-stu-id="55bb8-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="55bb8-131">Especificación de un BLOB en filtro</span><span class="sxs-lookup"><span data-stu-id="55bb8-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="55bb8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55bb8-132">Requirements</span></span>



| <span data-ttu-id="55bb8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="55bb8-133">Requirement</span></span> | <span data-ttu-id="55bb8-134">Value</span><span class="sxs-lookup"><span data-stu-id="55bb8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55bb8-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55bb8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="55bb8-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55bb8-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55bb8-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55bb8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="55bb8-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55bb8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55bb8-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55bb8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bb8-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="55bb8-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="55bb8-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55bb8-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="55bb8-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55bb8-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="55bb8-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55bb8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bb8-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bb8-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55bb8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="55bb8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bb8-146">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="55bb8-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="55bb8-147">SelectNPPBlobFromTable</span><span class="sxs-lookup"><span data-stu-id="55bb8-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




