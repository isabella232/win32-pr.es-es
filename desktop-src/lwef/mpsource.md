---
title: Enumeración MPSOURCE (MpClient.h)
description: Categoría posible de origen.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Enumeración MPSOURCE Características heredadas Windows entorno de ejecución
- Puntero de enumeración PMPSOURCE Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269463"
---
# <a name="mpsource-enumeration"></a>Enumeración MPSOURCE

Categoría posible de origen.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ UNKNOWN**
</dt> <dd>

Origen desconocido.

</dd> <dt>

<span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**USUARIO DE \_ MPSOURCE**
</dt> <dd>

Iniciado por el usuario.

</dd> <dt>

<span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**SISTEMA \_ MPSOURCE**
</dt> <dd>

iniciado por el sistema.

</dd> <dt>

<span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE \_ REALTIME**
</dt> <dd>

Componente en tiempo real iniciado.

</dd> <dt>

<span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE \_ IOAV**
</dt> <dd>

Descargas de IE y Outlook datos adjuntos rápidos iniciados.

</dd> <dt>

<span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE \_ NIS**
</dt> <dd>

Sistema de inspección de red.

</dd> <dt>

<span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE \_ BHO**
</dt> <dd>

BHO: script web (en desuso).

</dd> <dt>

<span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE \_ IEPROTECT**
</dt> <dd>

IE: IExtensionValidation.

</dd> <dt>

<span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE \_ ELAM**
</dt> <dd>

ELAM

</dd> <dt>

<span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**\_ATESTACIÓN LOCAL \_ DE MPSOURCE**
</dt> <dd>

Atestación local.

</dd> <dt>

<span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**\_ATESTACIÓN REMOTA \_ DE MPSOURCE**
</dt> <dd>

Atestación remota.

</dd> <dt>

<span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE \_ AMSI**
</dt> <dd>

AMSI

</dd> <dt>

<span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP \_ SOURCE \_ MAXVALUE**
</dt> <dd>

Valor máximo posible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





