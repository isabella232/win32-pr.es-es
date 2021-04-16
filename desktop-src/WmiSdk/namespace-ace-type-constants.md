---
description: Campo de tipo de una entrada de control de acceso (ACE) que determina si la ACE es una ACE que permite el acceso o deniega el acceso.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Constantes de tipo ACE de espacio de nombres (Winnt. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650085"
---
# <a name="namespace-ace-type-constants"></a>Constantes de tipo ACE de espacio de nombres

Campo de **tipo** de una entrada de control de acceso (ACE) que determina si la ACE es una ACE que permite el acceso o deniega el acceso.

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Ceda**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



La ACE permite el acceso al espacio de nombres.


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Impedir**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



La ACE deniega el acceso al espacio de nombres.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




