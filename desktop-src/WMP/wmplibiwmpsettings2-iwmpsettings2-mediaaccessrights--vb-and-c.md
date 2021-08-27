---
title: Propiedad IWMPSettings2 mediaAccessRights
description: La propiedad mediaAccessRights obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Propiedad mediaAccessRights Reproductor de Windows Media
- Propiedad mediaAccessRights Reproductor de Windows Media , interfaz IWMPSettings2
- Interfaz IWMPSettings2 Reproductor de Windows Media , propiedad mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 797e45c62b505033afd2126f79d5830de5bc9847a4de36199a6c919a4978f112
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122495"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>Propiedad IWMPSettings2::mediaAccessRights

La **propiedad mediaAccessRights** obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es uno de los valores siguientes.



| Value | Descripción                      |
|-------|----------------------------------|
| ninguno  | Solo derechos de acceso de elementos actuales. |
| leer  | Solo derechos de acceso de lectura.         |
| full  | Derechos de acceso de lectura y escritura.        |



 

## <a name="remarks"></a>Comentarios

Una página web debe solicitar primero permiso al usuario para leer información o escribir datos en la biblioteca. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso adecuados. Para obtener derechos de acceso, la aplicación llama a **IWMPSettings2.get \_ requestMediaAccessRights** y pasa un parámetro que especifica el nivel de derechos de acceso deseado.

Las aplicaciones que se ejecutan en el equipo del usuario siempre tienen derechos de acceso completos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





