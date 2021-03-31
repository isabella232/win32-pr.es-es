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
# <a name="dot11_phy_type-enumeration"></a>\_Enumeración de tipo PHY de DOT11 \_

La enumeración de **\_ \_ tipo PHY de DOT11** define un PHY 802,11 y un tipo de medio.

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

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**tipo de PHY de dot11 \_ \_ \_ desconocido**
</dt> <dd>

Especifica un tipo de PHY desconocido o no inicializado.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**tipo de PHY de dot11 \_ \_ \_ any**
</dt> <dd>

Especifica cualquier tipo de PHY.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**tipo de PHY de dot11 \_ \_ \_ FHSS**
</dt> <dd>

Especifica un PHY de espectro de distribución de salto de frecuencia (FHSS). Los dispositivos Bluetooth pueden usar FHSS o una adaptación de FHSS.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**\_DSSS de \_ tipo \_ PHY de dot11**
</dt> <dd>

Especifica un tipo de PHY de espectro de difusión de secuencia directa (DSSS).

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**tipo de PHY de dot11 \_ \_ \_ irbaseband**
</dt> <dd>

Especifica un tipo de PHY de banda (IR) de infrarrojos.

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**tipo de PHY de dot11 \_ \_ \_ OFDM**
</dt> <dd>

Especifica un tipo de PHY de multiplexación de división de frecuencia ortogonal (OFDM). 802.11 los dispositivos pueden usar OFDM.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**tipo de PHY de dot11 \_ \_ \_ hrdsss**
</dt> <dd>

Especifica un tipo de PHY de DSSS (HRDSSS) de alta frecuencia.

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**tipo de PHY de dot11 \_ \_ \_ ERP**
</dt> <dd>

Especifica un tipo de PHY de velocidad extendida (ERP). los dispositivos 802.11 g pueden usar ERP.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**\_tipo de PHY de dot11 \_ \_**
</dt> <dd>

Especifica el tipo de PHY de 802.11 n.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**tipo de PHY de dot11 \_ \_ \_ VHT**
</dt> <dd>

Especifica el tipo de PHY de AC 802.11. Este es el tipo de PHY de rendimiento muy alto especificado en IEEE 802.11 AC.

Este valor es compatible con Windows 8.1, Windows Server 2012 R2 y versiones posteriores.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_Inicio de \_ IHV de tipo PHY \_ de dot11 \_**
</dt> <dd>

Especifica el inicio del intervalo que se usa para definir los tipos de PHY desarrollados por un fabricante de hardware independiente (IHV).

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**tipo de PHY de dot11 \_ \_ \_ \_ -fin de IHV**
</dt> <dd>

Especifica el inicio del intervalo que se usa para definir los tipos de PHY desarrollados por un fabricante de hardware independiente (IHV).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un IHV puede asignar un valor para sus tipos de PHY de propiedad desde el tipo de PHY de **dot11 \_ \_ \_ \_ Inicio** a través del **\_ \_ tipo \_ \_ PHY de dot11**. El IHV debe asignar un número único de este intervalo para cada uno de sus tipos de PHY de propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Windot11. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**atributos de la Asociación de WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**funcionalidad de la interfaz de WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




