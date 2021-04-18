---
description: En la lista siguiente se enumeran los posibles valores del campo Flags en una entrada de Access Control WMI (ACE).
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes de marca ACE de espacio de nombres (Winnt. h)
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
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650086"
---
# <a name="namespace-ace-flag-constants"></a>Constantes de marca ACE de espacio de nombres

En la lista siguiente se enumeran los posibles valores del campo **Flags** en una entrada de Access Control WMI (ACE).

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**\_ACE de herencia de objeto \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Los objetos secundarios que no son de contenedor heredan la ACE como una ACE efectiva.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**\_ACE de herencia de contenedor \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



La ACE tiene un efecto en los espacios de nombres secundarios, así como en el espacio de nombres actual.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO \_ propagar \_ ACE de herencia \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



La ACE solo se aplica al espacio de nombres actual y a los elementos secundarios inmediatos.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**solo HEREDAr \_ \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



La ACE solo se aplica a los espacios de nombres secundarios.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**ACE HEREDAda \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



No lo establecen los clientes, pero se envía a los clientes cuando el origen de una ACE es un espacio de nombres primario.


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

 

 




