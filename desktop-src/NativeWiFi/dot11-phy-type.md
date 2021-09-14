---
description: Define un PHY 802.11 y un tipo de medio.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: DOT11_PHY_TYPE enumeración (Windot11.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071609"
---
# <a name="dot11_phy_type-enumeration"></a>Enumeración \_ PHY TYPE de DOT11 \_

La **enumeración \_ DOT11 PHY \_ TYPE** define un PHY 802.11 y un tipo de medio.

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**Dot11 \_ phy \_ type \_ unknown**
</dt> <dd>

Especifica un tipo PHY desconocido o no inicializado.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ phy \_ type \_ any**
</dt> <dd>

Especifica cualquier tipo PHY.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ phy \_ type \_ fhss**
</dt> <dd>

Especifica un PHY de intervalo de propagación de salto de frecuencia (FHSS). Bluetooth dispositivos pueden usar FHSS o una adaptación de FHSS.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ phy \_ type \_ dsss**
</dt> <dd>

Especifica un tipo PHY de espectro de propagación de secuencia directa (DSSS).

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ phy \_ type \_ irbaseband**
</dt> <dd>

Especifica un tipo PHY de banda base (IR).

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**Tipo \_ phy dot11 \_ \_ dedm**
</dt> <dd>

Especifica un tipo PHY de multiplexación de división de frecuencia ortogonal (OFDM). Los dispositivos 802.11a pueden usar OFDM.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ phy \_ type \_ hrdsss**
</dt> <dd>

Especifica un tipo PHY DSSS (HRDSSS) de alta velocidad.

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11 \_ phy \_ type \_ erp**
</dt> <dd>

Especifica un tipo PHY de velocidad extendida (ERP). Los dispositivos 802.11g pueden usar ERP.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ phy \_ type \_ ht**
</dt> <dd>

Especifica el tipo PHY 802.11n.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**vht \_ de tipo phy \_ \_ dot11**
</dt> <dd>

Especifica el tipo PHY 802.11ac. Este es el tipo PHY de rendimiento muy alto especificado en IEEE 802.11ac.

Este valor se admite en Windows 8.1, Windows Server 2012 R2 y versiones posteriores.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**Inicio de \_ IHV de tipo \_ \_ phy dot11 \_**
</dt> <dd>

Especifica el inicio del intervalo que se usa para definir tipos PHY desarrollados por un proveedor de hardware independiente (IHV).

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**Dot11 \_ phy \_ type \_ IHV \_ end**
</dt> <dd>

Especifica el inicio del intervalo que se usa para definir tipos PHY desarrollados por un proveedor de hardware independiente (IHV).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un IHV puede asignar un valor para sus tipos PHY propietarios desde **dot11 \_ phy \_ type \_ IHV \_ start** hasta **dot11 \_ phy \_ type \_ IHV \_ end**. El IHV debe asignar un número único de este intervalo para cada uno de sus tipos PHY propietarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Windot11.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ATRIBUTOS DE \_ ASOCIACIÓN DE WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**FUNCIONALIDAD \_ DE LA INTERFAZ \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




