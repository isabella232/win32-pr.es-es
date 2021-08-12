---
title: Configuración.requestMediaAccessRights (método)
description: El método requestMediaAccessRights solicita un nivel de acceso especificado a la biblioteca. | Configuración.requestMediaAccessRights (método)
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Método requestMediaAccessRights Reproductor de Windows Media
- Método requestMediaAccessRights Reproductor de Windows Media , Configuración clase
- Configuración clase Reproductor de Windows Media método , requestMediaAccessRights
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
ms.openlocfilehash: 1e157e7b4495c8d90964d62a9045eebb202126906f0022e97c4983220e47ac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569316"
---
# <a name="settingsrequestmediaaccessrights-method"></a>Configuración.requestMediaAccessRights (método)

El **método requestMediaAccessRights** solicita un nivel de acceso especificado a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*acceso* \[ En\]
</dt> <dd>

**Cadena** que especifica el nivel de derechos de acceso deseado. Contiene uno de los valores siguientes.



| String | Descripción                      |
|--------|----------------------------------|
| ninguno   | Solo derechos de acceso de elementos actuales. |
| leer   | Solo derechos de acceso de lectura.         |
| full   | Derechos de acceso de lectura y escritura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano** que indica si se han concedido los derechos de acceso solicitados.

## <a name="remarks"></a>Comentarios

En primer lugar, una página web debe solicitar permiso al usuario para leer o escribir datos en la biblioteca. Al invocar este método se solicita al usuario un cuadro de diálogo que solicita el nivel de permiso especificado. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso adecuados. El nivel de derechos de acceso actual se puede recuperar mediante *Configuración*. **mediaAccessRights**.

**Reproductor de Windows Media 10 Mobile:** este método siempre devuelve **true.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





