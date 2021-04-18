---
description: Identifica el tipo de host del llamador WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Enumeración WLDP_HOST_ID (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538344"
---
# <a name="wldp_host_id-enumeration"></a>\_ \_ Enumeración de ID. de host de WLDP

Identifica el tipo de host del llamador WLDP.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ identificador de HOST \_ \_ desconocido** 
</dt> <dd>

No se conoce el tipo de host.

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ \_ID. \_ de host global**
</dt> <dd>

El tipo de host es una directiva global.

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**identificador de host de WLDP \_ \_ \_ VBA**
</dt> <dd>

El tipo de host es VBScript.

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ \_ \_ WSH ID de host**
</dt> <dd>

El tipo de host es Windows Script Host.

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_ \_ POWERSHELL de ID. de host**
</dt> <dd>

El tipo de host es Windows PowerShell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_ID. \_ de host IE**
</dt> <dd>

El tipo de host es Internet Explorer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_ \_ MSI de ID. de host**
</dt> <dd>

El tipo de host es el Microsoft Windows Installer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_ID. \_ de host máximo** 
</dt> <dd>

Valor de enumeración máximo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl> |



 

 




