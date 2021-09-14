---
description: Indica si la conexión a una LAN inalámbrica debe ser automática o iniciada por el usuario.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento connectionMode (WLANProfile)
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
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245559"
---
# <a name="connectionmode-wlanprofile-element"></a>Elemento connectionMode (WLANProfile)

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

## <a name="remarks"></a>Observaciones

En la tabla siguiente se describen los valores de enumeración.



| Value  | Descripción                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | La conexión a la red inalámbrica debe iniciarse automáticamente siempre que la red esté dentro del intervalo. |
| manual | La conexión a la red inalámbrica solo se establece tras la solicitud explícita de un usuario.               |



 

## <a name="examples"></a>Ejemplos

Para ver perfiles de ejemplo que usan el **elemento connectionMode,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
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

 

 




