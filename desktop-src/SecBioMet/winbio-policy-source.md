---
title: WINBIO_POLICY_SOURCE enumeración (Winbio \_ types.h)
description: Enumera los posibles orígenes de información de directiva para la detección de suplantación de datos para factores biométricos.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE enumeración Windows Biometric Framework API
- PWINBIO_POLICY_SOURCE puntero de enumeración Windows BIOMETRIC Framework API
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
ms.openlocfilehash: 962d4bc3e8cffb778df56d78a9ddaf0641f57f8f96c8f7b024745a4b879f2f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909944"
---
# <a name="winbio_policy_source-enumeration"></a>Enumeración \_ WINBIO POLICY \_ SOURCE

Enumera los posibles orígenes de información de directiva para la detección de suplantación de datos para factores biométricos.

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

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**DIRECTIVA WINBIO \_ \_ DESCONOCIDA**
</dt> <dd>

Se desconoce el origen de la directiva.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**DIRECTIVA PREDETERMINADA DE WINBIO \_ \_**
</dt> <dd>

La directiva es la directiva predeterminada que proporciona Windows Biometric Framework.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**DIRECTIVA LOCAL DE WINBIO \_ \_**
</dt> <dd>

Directiva que el usuario individual estableció para su cuenta mediante el uso de **Configuración** aplicación. Esta directiva invalida la directiva predeterminada.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**ADMINISTRADOR DE DIRECTIVAS DE WINBIO \_ \_**
</dt> <dd>

Una directiva de grupo que el administrador de TI estableció para la empresa. Los usuarios individuales no pueden invalidar esta directiva.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACCIÓN DE \_ DIRECTIVA \_ ANTI SUPLANTACIÓN \_ DE SEGURIDAD DE \_ WINBIO**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





