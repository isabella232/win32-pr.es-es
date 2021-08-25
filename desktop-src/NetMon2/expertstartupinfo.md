---
description: Contiene datos que describen a un experto cuando se inicia.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Estructura EXPERTSTARTUPINFO (Netmon.h)
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
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911055"
---
# <a name="expertstartupinfo-structure"></a>ESTRUCTURA EXPERTSTARTUPINFO

La **estructura EXPERTSTARTUPINFO** contiene datos que describen a un experto cuando se inicia.

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

Marcas que describen al experto.

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

Número de fotograma.

</dd> <dt>

**hProtocol**
</dt> <dd>

Controle el protocolo.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Puntero a una [**estructura PROPERTYINST.**](propertyinst.md)

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

Solo se usa si el **miembro DataQualifier** de la [**estructura PROPERTYINST**](propertyinst.md) está establecido en PROP \_ QUAL \_ FLAGS.

</dd> <dt>

**Bon**
</dt> <dd>

Solo se usa si el **miembro DataQualifier** de la [**estructura PROPERTYINST**](propertyinst.md) está establecido en PROP \_ QUAL \_ FLAGS.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




