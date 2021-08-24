---
description: Indica si la conexión a una LAN inalámbrica debe ser automática o iniciada por el usuario.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: elemento connectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a6ef18eff8ba27a3169399f1f10e0707c4e0b3c010d54830ad8f8f997c5e1b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684445"
---
# <a name="connectionmode-wlanprofile-element"></a>elemento connectionMode (WLANProfile)

El elemento connectionMode (WLANProfile) indica si la conexión a una LAN inalámbrica debe ser automática o iniciada por el usuario.

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en ESS, este valor puede ser automático o manual. El valor predeterminado es auto si este elemento no está presente.

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en IBSS, este valor debe ser manual.

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento connectionMode** se define mediante el [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="remarks"></a>Comentarios

En la tabla siguiente se describen los valores de enumeración.



| Valor  | Descripción                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | La conexión a la red inalámbrica debe iniciarse automáticamente siempre que la red esté dentro del alcance. |
| manual | La conexión a la red inalámbrica solo se establece tras la solicitud explícita de un usuario.               |



 

## <a name="examples"></a>Ejemplos

Para ver perfiles de ejemplo que usan el **elemento connectionMode,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




