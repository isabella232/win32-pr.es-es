---
title: Estructura de MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: La \_ estructura MCI OVLY \_ Open \_ parms contiene información del comando MCI \_ Open para dispositivos de superposición de vídeo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Estructura de MCI_OVLY_OPEN_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488987"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="896ed-104">MCI \_ OVLY \_ Open \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="896ed-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="896ed-105">La estructura **MCI \_ OVLY \_ Open \_ parms** contiene información del comando [**MCI \_ Open**](mci-open.md) para dispositivos de superposición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="896ed-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="896ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="896ed-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="896ed-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="896ed-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="896ed-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="896ed-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="896ed-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="896ed-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="896ed-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-111">Identificador devuelto a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="896ed-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="896ed-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="896ed-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-113">Nombre o identificador constante del tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="896ed-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="896ed-114">(El nombre del dispositivo normalmente se obtiene del registro o del archivo de SYSTEM.INI). Si este miembro es una constante, puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="896ed-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="896ed-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="896ed-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-116">Nombre del elemento de dispositivo (normalmente una ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="896ed-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="896ed-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="896ed-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-118">Alias de dispositivo opcional.</span><span class="sxs-lookup"><span data-stu-id="896ed-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="896ed-119">**dwStyle**</span><span class="sxs-lookup"><span data-stu-id="896ed-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-120">Estilo de ventana.</span><span class="sxs-lookup"><span data-stu-id="896ed-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="896ed-121">**hWndParent**</span><span class="sxs-lookup"><span data-stu-id="896ed-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="896ed-122">Identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="896ed-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="896ed-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="896ed-123">Remarks</span></span>

<span data-ttu-id="896ed-124">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="896ed-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="896ed-125">Puede usar la estructura [**MCI \_ Open \_ parms**](mci-open-parms.md) en lugar de **MCI \_ OVLY \_ Open \_ parms** si no está usando los miembros de datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="896ed-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="896ed-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="896ed-126">Requirements</span></span>



| <span data-ttu-id="896ed-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="896ed-127">Requirement</span></span> | <span data-ttu-id="896ed-128">Value</span><span class="sxs-lookup"><span data-stu-id="896ed-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="896ed-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="896ed-129">Minimum supported client</span></span><br/> | <span data-ttu-id="896ed-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="896ed-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="896ed-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="896ed-131">Minimum supported server</span></span><br/> | <span data-ttu-id="896ed-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="896ed-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="896ed-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="896ed-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="896ed-134"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="896ed-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="896ed-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="896ed-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896ed-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="896ed-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="896ed-137">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="896ed-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="896ed-138">**MCI \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="896ed-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="896ed-139">**MCI \_ abierto \_ parms**</span><span class="sxs-lookup"><span data-stu-id="896ed-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="896ed-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="896ed-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

