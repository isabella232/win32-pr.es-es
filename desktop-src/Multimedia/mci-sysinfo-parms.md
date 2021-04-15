---
title: MCI_SYSINFO_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura de parms de MCI sysinfo contiene información para el comando de MCI \_ sysinfo.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Estructura de MCI_SYSINFO_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676555"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="7f954-104">\_ \_ Estructura parms de MCI SYSINFO</span><span class="sxs-lookup"><span data-stu-id="7f954-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="7f954-105">La estructura de **\_ \_ parms de MCI sysinfo** contiene información para el comando de [**MCI \_ sysinfo**](mci-sysinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7f954-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f954-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f954-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="7f954-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f954-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f954-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="7f954-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="7f954-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7f954-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="7f954-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="7f954-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="7f954-111">Puntero a un búfer proporcionado por el usuario para la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="7f954-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="7f954-112">También se usa para devolver un valor **DWORD** cuando \_ se usa la marca de cantidad de MCI SYSINFO \_ .</span><span class="sxs-lookup"><span data-stu-id="7f954-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="7f954-113">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="7f954-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="7f954-114">Tamaño, en bytes, del búfer de retorno.</span><span class="sxs-lookup"><span data-stu-id="7f954-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7f954-115">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="7f954-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="7f954-116">Número que indica la posición del dispositivo en la tabla de dispositivos MCI o en la lista de dispositivos abiertos \_ si \_ se establece la marca de apertura de MCI SYSINFO.</span><span class="sxs-lookup"><span data-stu-id="7f954-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="7f954-117">**wDeviceType**</span><span class="sxs-lookup"><span data-stu-id="7f954-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="7f954-118">Tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f954-118">Type of device.</span></span> <span data-ttu-id="7f954-119">Este miembro puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="7f954-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f954-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f954-120">Remarks</span></span>

<span data-ttu-id="7f954-121">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="7f954-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f954-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f954-122">Requirements</span></span>



| <span data-ttu-id="7f954-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f954-123">Requirement</span></span> | <span data-ttu-id="7f954-124">Value</span><span class="sxs-lookup"><span data-stu-id="7f954-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f954-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f954-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f954-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7f954-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f954-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f954-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f954-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f954-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f954-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f954-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f954-130"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f954-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f954-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f954-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f954-132">**MCI**</span><span class="sxs-lookup"><span data-stu-id="7f954-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7f954-133">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="7f954-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="7f954-134">**MCI \_ SYSINFO**</span><span class="sxs-lookup"><span data-stu-id="7f954-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="7f954-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f954-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

