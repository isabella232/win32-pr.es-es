---
title: Settings. requestMediaAccessRights (método)
description: El método requestMediaAccessRights solicita un nivel de acceso especificado a la biblioteca. | Settings. requestMediaAccessRights (método)
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- método requestMediaAccessRights de Windows Media Player
- método requestMediaAccessRights de Windows Media Player, clase de configuración
- Clase de configuración Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653572"
---
# <a name="settingsrequestmediaaccessrights-method"></a>Settings. requestMediaAccessRights (método)

El método **requestMediaAccessRights** solicita un nivel de acceso especificado a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*acceso a* \[ de\]
</dt> <dd>

**Cadena** que especifica el nivel de derechos de acceso deseado. Contiene uno de los valores siguientes.



| String | Descripción                      |
|--------|----------------------------------|
| ninguno   | Solo los derechos de acceso a elementos actuales. |
| leer   | Solo derechos de acceso de lectura.         |
| full   | Derechos de acceso de lectura y escritura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un valor **booleano** que indica si se concedieron los derechos de acceso solicitados.

## <a name="remarks"></a>Observaciones

Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca. Al invocar este método, se solicita al usuario un cuadro de diálogo que solicita el nivel de permiso especificado. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes. El nivel de derechos de acceso actual se puede recuperar mediante la *configuración*. **mediaAccessRights**.

**Windows Media Player 10 Mobile**: este método siempre devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





