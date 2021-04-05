---
title: Enumeración WINBIO_POLICY_SOURCE (Winbio \_ Types. h)
description: Enumera los orígenes posibles de información de directiva para la detección de suplantación de los factores biométricos.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE enumeración Plataforma de biometría de Windows API
- PWINBIO_POLICY_SOURCE de puntero de enumeración Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359851"
---
# <a name="winbio_policy_source-enumeration"></a>\_Enumeración de origen de directiva WINBIO \_

Enumera los orígenes posibles de información de directiva para la detección de suplantación de los factores biométricos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**Directiva de WINBIO \_ \_ desconocida**
</dt> <dd>

Se desconoce el origen de la Directiva.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_directiva \_ predeterminada de WINBIO**
</dt> <dd>

La Directiva es la directiva predeterminada que proporciona el Plataforma de biometría de Windows.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_Directiva WINBIO \_ local**
</dt> <dd>

La directiva establecida por el usuario individual para su cuenta mediante la aplicación de **configuración** . Esta directiva invalida la directiva predeterminada.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_Administrador de directivas de WINBIO \_**
</dt> <dd>

Una directiva de grupo establecida por el administrador de TI para la empresa. Los usuarios individuales no pueden invalidar esta Directiva.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**acción de directiva de WINBIO \_ anti \_ Spoofing \_ \_**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





