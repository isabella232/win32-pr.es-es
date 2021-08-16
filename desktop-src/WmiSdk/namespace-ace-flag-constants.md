---
description: En la lista siguiente se enumeran los valores posibles del campo Marcas en una entrada Access Control WMI (ACE).
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes de marca ACE de espacio de nombres (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 7b4051a6c17e9861d656207335b2543cf7d886e74569c269df2a4f680f47fbe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555185"
---
# <a name="namespace-ace-flag-constants"></a>Constantes de marca ACE de espacio de nombres

En la lista siguiente se enumeran los valores **posibles** del campo Marcas en una entrada Access Control WMI (ACE).

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**ACE \_ DE HERENCIA DE \_ OBJETO**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Los objetos secundarios que no son contenedores heredan la ACE como una ACE efectiva.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**ACE \_ DE HERENCIA DE \_ CONTENEDOR**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



La ACE tiene un efecto en los espacios de nombres secundarios, así como en el espacio de nombres actual.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO \_ PROPAGATE \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



La ACE solo se aplica al espacio de nombres actual y a los secundarios inmediatos.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**HEREDAR \_ SOLO \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



La ACE solo se aplica a los espacios de nombres secundarios.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**ACE \_ HEREDADA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Los clientes no lo establecen, pero se notifica a los clientes cuando el origen de una ACE es un espacio de nombres primario.


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

 

 




