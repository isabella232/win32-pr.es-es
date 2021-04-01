---
title: MCI_OPEN_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI Open \_ parms contiene información para el \_ comando MCI Open.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- Estructura de MCI_OPEN_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150174"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="b6dfb-104">\_Estructura parms abierta de MCI \_</span><span class="sxs-lookup"><span data-stu-id="b6dfb-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="b6dfb-105">La estructura **MCI \_ Open \_ parms** contiene información para el comando [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b6dfb-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6dfb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6dfb-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="b6dfb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6dfb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6dfb-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b6dfb-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b6dfb-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b6dfb-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="b6dfb-111">Identificador devuelto a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6dfb-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="b6dfb-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="b6dfb-113">Nombre o identificador constante del tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6dfb-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="b6dfb-114">(El nombre del dispositivo normalmente se obtiene del registro o del archivo de SYSTEM.INI). Si este miembro es una constante, puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="b6dfb-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6dfb-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="b6dfb-116">Elemento de dispositivo (suele ser una ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="b6dfb-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="b6dfb-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="b6dfb-118">Alias de dispositivo opcional.</span><span class="sxs-lookup"><span data-stu-id="b6dfb-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6dfb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6dfb-119">Remarks</span></span>

<span data-ttu-id="b6dfb-120">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="b6dfb-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6dfb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6dfb-121">Requirements</span></span>



| <span data-ttu-id="b6dfb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6dfb-122">Requirement</span></span> | <span data-ttu-id="b6dfb-123">Value</span><span class="sxs-lookup"><span data-stu-id="b6dfb-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dfb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6dfb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6dfb-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b6dfb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b6dfb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6dfb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6dfb-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6dfb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b6dfb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6dfb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6dfb-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6dfb-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6dfb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6dfb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6dfb-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b6dfb-132">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b6dfb-133">**MCI \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="b6dfb-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="b6dfb-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6dfb-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

