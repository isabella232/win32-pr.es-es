---
title: Enumeración MP_SIGNATURE_TYPE (MpClient. h)
description: Posibles tipos de firma.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE enumeración características de entorno heredado de Windows
- PMP_SIGNATURE_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490396"
---
# <a name="mp_signature_type-enumeration"></a>\_Enumeración de tipos de firma de MP \_

Posibles tipos de firma.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**antimalware de firma de MP \_ \_**
</dt> <dd>

Firmas antivirus y antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**\_antivirus de firmas de MP \_**
</dt> <dd>

Solo firmas de antivirus.

</dd> <dt>

<span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**\_AntiSpyware de firma de MP \_**
</dt> <dd>

Solo firmas de anti spyware.

</dd> <dt>

<span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**firma de MP en \_ \_ NIS**
</dt> <dd>

Firmas NIS.

</dd> <dt>

<span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**tipos de firma de MP \_ \_ \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





