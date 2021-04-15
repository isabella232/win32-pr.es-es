---
title: MCI_WAVE_OPEN_PARMS estructura (Mciapi. h)
description: La estructura de parms de MCI \_ \_ Open Wave \_ contiene información para el \_ comando MCI Open para dispositivos de audio de forma de onda.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Estructura de MCI_WAVE_OPEN_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676861"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="05d3c-104">\_ \_ Estructura parms de MCI Open Wave \_</span><span class="sxs-lookup"><span data-stu-id="05d3c-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="05d3c-105">La estructura de **parms de MCI \_ \_ Open \_ Wave** contiene información para el comando [**MCI \_ Open**](mci-open.md) para dispositivos de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="05d3c-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d3c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05d3c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="05d3c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="05d3c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="05d3c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="05d3c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="05d3c-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="05d3c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="05d3c-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="05d3c-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="05d3c-111">Identificador devuelto a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="05d3c-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="05d3c-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="05d3c-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="05d3c-113">Nombre o identificador constante del tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05d3c-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="05d3c-114">(El nombre del dispositivo normalmente se obtiene del registro o del archivo de SYSTEM.INI). Este miembro puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="05d3c-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="05d3c-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="05d3c-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="05d3c-116">Nombre del elemento de dispositivo (normalmente una ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="05d3c-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="05d3c-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="05d3c-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="05d3c-118">Alias de dispositivo opcional.</span><span class="sxs-lookup"><span data-stu-id="05d3c-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="05d3c-119">**dwBufferSeconds**</span><span class="sxs-lookup"><span data-stu-id="05d3c-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="05d3c-120">Longitud del búfer, en segundos.</span><span class="sxs-lookup"><span data-stu-id="05d3c-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05d3c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05d3c-121">Remarks</span></span>

<span data-ttu-id="05d3c-122">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="05d3c-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="05d3c-123">Puede usar la estructura [**MCI \_ Open \_ parms**](mci-open-parms.md) en lugar de **MCI \_ Wave \_ Open \_ parms** si no está usando los miembros de datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="05d3c-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d3c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05d3c-124">Requirements</span></span>



| <span data-ttu-id="05d3c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d3c-125">Requirement</span></span> | <span data-ttu-id="05d3c-126">Value</span><span class="sxs-lookup"><span data-stu-id="05d3c-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="05d3c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05d3c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="05d3c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="05d3c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="05d3c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05d3c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="05d3c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05d3c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="05d3c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05d3c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="05d3c-132"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="05d3c-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d3c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="05d3c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d3c-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="05d3c-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="05d3c-135">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="05d3c-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="05d3c-136">**MCI \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="05d3c-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="05d3c-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="05d3c-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="05d3c-138">**MCI \_ abierto \_ parms**</span><span class="sxs-lookup"><span data-stu-id="05d3c-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 

