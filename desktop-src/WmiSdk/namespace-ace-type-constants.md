---
description: Campo Tipo de una entrada de control de acceso (ACE) que determina si la ACE es una ACE que permite el acceso o deniega el acceso.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Constantes de tipo ACE de espacio de nombres (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172558"
---
# <a name="namespace-ace-type-constants"></a>Constantes de tipo ACE de espacio de nombres

Campo **Tipo** de una entrada de control de acceso (ACE) que determina si la ACE es una ACE que permite el acceso o deniega el acceso.

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Conceder**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



La ACE permite el acceso al espacio de nombres .


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Negar**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



La ACE deniega el acceso al espacio de nombres.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de seguridad WMI](wmi-security-constants.md)
</dt> <dt>

[Establecer descriptores de seguridad de namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




