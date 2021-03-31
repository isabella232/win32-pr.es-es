---
description: Define un PHY 802,11 y un tipo de medio.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: Enumeración DOT11_PHY_TYPE (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910654"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="3e4a7-103">\_Enumeración de tipo PHY de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="3e4a7-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="3e4a7-104">La enumeración de **\_ \_ tipo PHY de DOT11** define un PHY 802,11 y un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e4a7-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3e4a7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e4a7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e4a7-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**tipo de PHY de dot11 \_ \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-108">Especifica un tipo de PHY desconocido o no inicializado.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**tipo de PHY de dot11 \_ \_ \_ any**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-110">Especifica cualquier tipo de PHY.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**tipo de PHY de dot11 \_ \_ \_ FHSS**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-112">Especifica un PHY de espectro de distribución de salto de frecuencia (FHSS).</span><span class="sxs-lookup"><span data-stu-id="3e4a7-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="3e4a7-113">Los dispositivos Bluetooth pueden usar FHSS o una adaptación de FHSS.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**\_DSSS de \_ tipo \_ PHY de dot11**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-115">Especifica un tipo de PHY de espectro de difusión de secuencia directa (DSSS).</span><span class="sxs-lookup"><span data-stu-id="3e4a7-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**tipo de PHY de dot11 \_ \_ \_ irbaseband**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-117">Especifica un tipo de PHY de banda (IR) de infrarrojos.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**tipo de PHY de dot11 \_ \_ \_ OFDM**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-119">Especifica un tipo de PHY de multiplexación de división de frecuencia ortogonal (OFDM).</span><span class="sxs-lookup"><span data-stu-id="3e4a7-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="3e4a7-120">802.11 los dispositivos pueden usar OFDM.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**tipo de PHY de dot11 \_ \_ \_ hrdsss**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-122">Especifica un tipo de PHY de DSSS (HRDSSS) de alta frecuencia.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**tipo de PHY de dot11 \_ \_ \_ ERP**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-124">Especifica un tipo de PHY de velocidad extendida (ERP).</span><span class="sxs-lookup"><span data-stu-id="3e4a7-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="3e4a7-125">los dispositivos 802.11 g pueden usar ERP.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**\_tipo de PHY de dot11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-127">Especifica el tipo de PHY de 802.11 n.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**tipo de PHY de dot11 \_ \_ \_ VHT**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-129">Especifica el tipo de PHY de AC 802.11.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="3e4a7-130">Este es el tipo de PHY de rendimiento muy alto especificado en IEEE 802.11 AC.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="3e4a7-131">Este valor es compatible con Windows 8.1, Windows Server 2012 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_Inicio de \_ IHV de tipo PHY \_ de dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-133">Especifica el inicio del intervalo que se usa para definir los tipos de PHY desarrollados por un fabricante de hardware independiente (IHV).</span><span class="sxs-lookup"><span data-stu-id="3e4a7-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="3e4a7-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**tipo de PHY de dot11 \_ \_ \_ \_ -fin de IHV**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="3e4a7-135">Especifica el inicio del intervalo que se usa para definir los tipos de PHY desarrollados por un fabricante de hardware independiente (IHV).</span><span class="sxs-lookup"><span data-stu-id="3e4a7-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e4a7-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e4a7-136">Remarks</span></span>

<span data-ttu-id="3e4a7-137">Un IHV puede asignar un valor para sus tipos de PHY de propiedad desde el tipo de PHY de **dot11 \_ \_ \_ \_ Inicio** a través del **\_ \_ tipo \_ \_ PHY de dot11**.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="3e4a7-138">El IHV debe asignar un número único de este intervalo para cada uno de sus tipos de PHY de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e4a7-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e4a7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e4a7-139">Requirements</span></span>



| <span data-ttu-id="3e4a7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e4a7-140">Requirement</span></span> | <span data-ttu-id="3e4a7-141">Value</span><span class="sxs-lookup"><span data-stu-id="3e4a7-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4a7-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e4a7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3e4a7-143">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3e4a7-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="3e4a7-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e4a7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3e4a7-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e4a7-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e4a7-146">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3e4a7-146">Redistributable</span></span><br/>          | <span data-ttu-id="3e4a7-147">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="3e4a7-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="3e4a7-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e4a7-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e4a7-149"><dt>Windot11. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e4a7-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e4a7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e4a7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4a7-151">**atributos de la Asociación de WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="3e4a7-152">**funcionalidad de la interfaz de WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e4a7-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




