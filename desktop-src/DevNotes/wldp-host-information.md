---
description: Estructura que identifica el host y el archivo de origen que se va a evaluar.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION estructura (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: cc1bed8fd104b4aa6abb83d3eb7e19faa37a0301429312c8f0799e256ce32ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404074"
---
# <a name="wldp_host_information-structure"></a>Estructura DE \_ INFORMACIÓN DE HOST DE \_ WLDP

Estructura que identifica el host y el archivo de origen que se va a evaluar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwRevision**
</dt> <dd>

Debe ser **WLDP \_ HOST INFORMATION \_ \_ REVISION**.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valor de enumeración [**del \_ \_ id. de host de WLDP**](wldp-host-id.md) que describe el identificador de host.

</dd> <dt>

**szSource**
</dt> <dd>

Ruta de acceso completa y nombre de script con la extensión. NULL para **EL IDENTIFICADOR DE HOST DE WLDP \_ \_ \_ GLOBAL** o la ejecución manual de scripts.

</dd> <dt>

**hSource**
</dt> <dd>

Además del nombre, el autor de la llamada puede especificar un identificador para el archivo utilizado para la validación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl> |



 

 




