---
title: Identificadores de proveedor integrados (Fwpmu.h)
description: Los identificadores de los proveedores integrados en Windows Filtering Platform (WFP) se representan mediante un GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8982fe6ebbe3f4cf5135f2b67f07826ddf9d3f970ca0568c7095931c617cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951314"
---
# <a name="built-in-provider-identifiers"></a>Identificadores de proveedor integrados

Los identificadores de los proveedores integrados en Windows Filtering Platform (WFP) se representan mediante un GUID.

Estos identificadores se definen de la manera siguiente.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**IXT DEL \_ PROVEEDOR FWPM \_**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



Se usa para identificar todos los filtros agregados por IKE/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM \_ PROVIDER \_ IPSEC \_ DOS \_ CONFIG**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Se usa para identificar todos los filtros agregados por IPsec DoS Protection.

> [!Note]  
> Disponible solo en Windows 7 y Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**DESCARGA DE TCP \_ \_ CHIMNEY DEL PROVEEDOR FWPM \_ \_**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



Se usa para identificar todos los filtros agregados por descarga tcp-de-in-in-off.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**PLANTILLAS TCP DEL \_ PROVEEDOR \_ FWPM \_**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



Se usa para identificar todos los filtros agregados por las plantillas TCP.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





