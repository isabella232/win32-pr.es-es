---
description: Contiene datos que describen un experto cuando se inicia.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Estructura EXPERTSTARTUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000941"
---
# <a name="expertstartupinfo-structure"></a>Estructura EXPERTSTARTUPINFO

La estructura **EXPERTSTARTUPINFO** contiene datos que describen un experto cuando se inicia.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Marcas que describen el experto.

</dd> <dt>

**hCapture**
</dt> <dd>

Identificador de una captura.

</dd> <dt>

**szCaptureFile**
</dt> <dd>

Nombre del archivo de captura.

</dd> <dt>

**dwFrameNumber**
</dt> <dd>

Número de marco.

</dd> <dt>

**hProtocol**
</dt> <dd>

Identificador del protocolo.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Puntero a una estructura [**PROPERTYINST**](propertyinst.md) .

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

Solo se usa si el miembro de **calificador** de la estructura [**PROPERTYINST**](propertyinst.md) está establecido en las marcas propia \_ \_ .

</dd> <dt>

**Despedida**
</dt> <dd>

Solo se usa si el miembro de **calificador** de la estructura [**PROPERTYINST**](propertyinst.md) está establecido en las marcas propia \_ \_ .

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




