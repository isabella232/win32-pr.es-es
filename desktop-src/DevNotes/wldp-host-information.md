---
description: Estructura que identifica el host y el archivo de código fuente que se va a evaluar.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION estructura (WLDP. h)
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
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080105"
---
# <a name="wldp_host_information-structure"></a>Estructura de información de \_ host de WLDP \_

Estructura que identifica el host y el archivo de código fuente que se va a evaluar.

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

Debe ser **la \_ \_ \_ revisión de información del host de WLDP**.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valor de enumeración del [**\_ \_ ID**](wldp-host-id.md) . de host de WLDP que describe el identificador de host.

</dd> <dt>

**szSource**
</dt> <dd>

Ruta de acceso completa y nombre de script con la extensión. NULL para el ID. de **host de WLDP \_ \_ \_ global** o la ejecución de script manual.

</dd> <dt>

**hSource**
</dt> <dd>

Además del nombre, el llamador puede especificar un identificador para el archivo que se utiliza para la validación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl> |



 

 




