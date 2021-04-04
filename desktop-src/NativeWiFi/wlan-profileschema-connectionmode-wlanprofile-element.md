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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811467"
---
# <a name="connectionmode-wlanprofile-element"></a>Elemento connectionMode (WLANProfile)

El elemento connectionMode (WLANProfile) indica si la conexión a una LAN inalámbrica debe ser automática o iniciada por el usuario.

Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en ESS, este valor puede ser auto o manual. Si este elemento no está presente, el valor predeterminado es auto.

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

El elemento **connectionMode** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Observaciones

En la tabla siguiente se describen los valores de enumeración.



| Value  | Descripción                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | La conexión a la red inalámbrica debe iniciarse automáticamente cuando la red esté dentro del alcance. |
| manual | La conexión a la red inalámbrica solo se inicia en la solicitud explícita de un usuario.               |



 

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **connectionMode** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
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

 

 




